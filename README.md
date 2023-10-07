# Yeni
açık kaynak
import discord
from discord.ext import commands
from settings import settings

intents = discord.Intents.default()
intents.message_content = True

# Botunuzu oluşturun
bot = commands.Bot(command_prefix='!', intents=intents)

# Yardım komutunu oluşturun
@bot.command()
async def yardim(ctx):
    yardim_mesaji = """
    Merhaba Kardeş! Ben çevre dostu bir Discord botuyum. İşte kullanabileceğiniz komutlar. Buyur kullan:
    
    !bilgi - Çevre temizliği ve sürdürülebilirlik hakkında bilgi alın.
    !geri_donusum - Geri dönüşüm hakkında ipuçları alın.
    !enerji_tasarrufu - Enerji tasarrufu hakkında öneriler alın.
    """
    await ctx.send(yardim_mesaji)

# Bilgi komutunu oluşturun
@bot.command()
async def bilgi(ctx):
    bilgi_mesaji = "Wikipediadan bak! Bot olabilirim ama bir kalbim var... Kodlar yani."
    await ctx.send(bilgi_mesaji)

# Geri dönüşüm komutunu oluşturun
@bot.command()
async def geri_donusum(ctx):
    geri_donusum_mesaji = "Eğer Thanason Haklı olduğunu öğrenmek istemiyorsan şu dünyayı temizle... Abicim hadi kırma beni"
    await ctx.send(geri_donusum_mesaji)

@bot.command()
async def bagimlilik(ctx):
    bagimlilik_mesaji = "Bak aga sana diyeceğim tek birşey var... Babandan modemi almasını iste. ;)"
    await ctx.send(bagimlilik_mesaji)

@bot.command()
async def galatasaray(ctx):
    galatasaray_mesaji = "Manchester united'a böyle goller atarız! Re re re ra ra ra gasaray gasaray cimbombom!. ;)"
    await ctx.send(galatasaray_mesaji)

@bot.command()
async def wiliam(ctx):
    wiliam_mesaji = "... T_T ;)"
    await ctx.send(wiliam_mesaji)



# Enerji tasarrufu komutunu oluşturun
@bot.command()
async def enerji_tasarrufu(ctx):
    enerji_tasarrufu_mesaji = "Kullanmıyorsan elektronik aletleri kapat..."
    await ctx.send(enerji_tasarrufu_mesaji)

# Botunuzu çalıştırın
bot.run(settings['token1'])
