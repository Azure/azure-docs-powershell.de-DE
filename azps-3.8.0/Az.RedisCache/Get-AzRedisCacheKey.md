---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 5588a3abecdec741aa6630083c38c01178669bae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003775"
---
# <span data-ttu-id="95074-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="95074-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="95074-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="95074-102">SYNOPSIS</span></span>
<span data-ttu-id="95074-103">Ruft die Zugriffstasten für einen zwischen Speicherungs-Cache ab.</span><span class="sxs-lookup"><span data-stu-id="95074-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="95074-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="95074-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="95074-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95074-105">DESCRIPTION</span></span>
<span data-ttu-id="95074-106">Das Cmdlet " **Get-AzRedisCacheKey** " Ruft die Zugriffstasten für einen Azure-a/a-Cache ab.</span><span class="sxs-lookup"><span data-stu-id="95074-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="95074-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="95074-107">EXAMPLES</span></span>

### <span data-ttu-id="95074-108">Beispiel 1: Abrufen der Zugriffstasten für einen Zeichenfolgen-Cache</span><span class="sxs-lookup"><span data-stu-id="95074-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="95074-109">Dieser Befehl ruft die Zugriffstasten mit dem Namen MyCacheKey ab.</span><span class="sxs-lookup"><span data-stu-id="95074-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="95074-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="95074-110">PARAMETERS</span></span>

### <span data-ttu-id="95074-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95074-111">-DefaultProfile</span></span>
<span data-ttu-id="95074-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="95074-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95074-113">-Name</span><span class="sxs-lookup"><span data-stu-id="95074-113">-Name</span></span>
<span data-ttu-id="95074-114">Gibt den Namen eines a/a-Caches an.</span><span class="sxs-lookup"><span data-stu-id="95074-114">Specifies the name of a Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95074-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95074-115">-ResourceGroupName</span></span>
<span data-ttu-id="95074-116">Gibt den Namen der Ressourcengruppe an, die den Zwischenspeicher mit dem Namenzeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="95074-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95074-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95074-117">CommonParameters</span></span>
<span data-ttu-id="95074-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95074-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95074-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95074-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95074-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="95074-120">INPUTS</span></span>

### <span data-ttu-id="95074-121">System. String</span><span class="sxs-lookup"><span data-stu-id="95074-121">System.String</span></span>

## <span data-ttu-id="95074-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="95074-122">OUTPUTS</span></span>

### <span data-ttu-id="95074-123">Microsoft. Azure. Management. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="95074-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="95074-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="95074-124">NOTES</span></span>

## <span data-ttu-id="95074-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="95074-125">RELATED LINKS</span></span>

[<span data-ttu-id="95074-126">Neu – AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="95074-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)


