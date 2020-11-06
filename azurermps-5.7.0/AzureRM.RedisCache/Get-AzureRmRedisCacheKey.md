---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
ms.openlocfilehash: 67ec6bdcce5121c2a80e1f76ea1081f249f15682
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482802"
---
# <span data-ttu-id="0f449-101">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="0f449-101">Get-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="0f449-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0f449-102">SYNOPSIS</span></span>
<span data-ttu-id="0f449-103">Ruft die Zugriffstasten für einen zwischen Speicherungs-Cache ab.</span><span class="sxs-lookup"><span data-stu-id="0f449-103">Gets the access keys for a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f449-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f449-104">SYNTAX</span></span>

```
Get-AzureRmRedisCacheKey [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f449-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f449-105">DESCRIPTION</span></span>
<span data-ttu-id="0f449-106">Das Cmdlet " **Get-AzureRmRedisCacheKey** " Ruft die Zugriffstasten für einen Azure-a/a-Cache ab.</span><span class="sxs-lookup"><span data-stu-id="0f449-106">The **Get-AzureRmRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="0f449-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f449-107">EXAMPLES</span></span>

### <span data-ttu-id="0f449-108">Beispiel 1: Abrufen der Zugriffstasten für einen Zeichenfolgen-Cache</span><span class="sxs-lookup"><span data-stu-id="0f449-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzureRmRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="0f449-109">Dieser Befehl ruft die Zugriffstasten mit dem Namen MyCacheKey ab.</span><span class="sxs-lookup"><span data-stu-id="0f449-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="0f449-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f449-110">PARAMETERS</span></span>

### <span data-ttu-id="0f449-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f449-111">-DefaultProfile</span></span>
<span data-ttu-id="0f449-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0f449-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f449-113">-Name</span><span class="sxs-lookup"><span data-stu-id="0f449-113">-Name</span></span>
<span data-ttu-id="0f449-114">Gibt den Namen eines a/a-Caches an.</span><span class="sxs-lookup"><span data-stu-id="0f449-114">Specifies the name of a Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f449-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f449-115">-ResourceGroupName</span></span>
<span data-ttu-id="0f449-116">Gibt den Namen der Ressourcengruppe an, die den Zwischenspeicher mit dem Namenzeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="0f449-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f449-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f449-117">CommonParameters</span></span>
<span data-ttu-id="0f449-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f449-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f449-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f449-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f449-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0f449-120">INPUTS</span></span>

### <span data-ttu-id="0f449-121">Keine</span><span class="sxs-lookup"><span data-stu-id="0f449-121">None</span></span>
<span data-ttu-id="0f449-122">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="0f449-122">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="0f449-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0f449-123">OUTPUTS</span></span>

### <span data-ttu-id="0f449-124">Microsoft. Azure. Management. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="0f449-124">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>
<span data-ttu-id="0f449-125">Dieses Cmdlet gibt die primären und sekundären Zugriffstasten für einen 4-a-Cache zurück.</span><span class="sxs-lookup"><span data-stu-id="0f449-125">This cmdlet returns primary and secondary access keys for a Redis Cache.</span></span>

## <span data-ttu-id="0f449-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="0f449-126">NOTES</span></span>

## <span data-ttu-id="0f449-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0f449-127">RELATED LINKS</span></span>

[<span data-ttu-id="0f449-128">Neu – AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="0f449-128">New-AzureRmRedisCacheKey</span></span>](./New-AzureRmRedisCacheKey.md)


