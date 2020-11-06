---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
ms.openlocfilehash: d54bc01e7a5aa23206037d4eb1d99e5d9e5deb0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501102"
---
# <span data-ttu-id="75327-101">New-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="75327-101">New-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="75327-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75327-102">SYNOPSIS</span></span>
<span data-ttu-id="75327-103">Regeneriert die Zugriffstaste eines a/a-Caches.</span><span class="sxs-lookup"><span data-stu-id="75327-103">Regenerates the access key of a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75327-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75327-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75327-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75327-105">DESCRIPTION</span></span>
<span data-ttu-id="75327-106">Mit dem Cmdlet **New-AzureRmRedisCacheKey** wird die Zugriffstaste eines Azure-a/a-Caches neu generiert.</span><span class="sxs-lookup"><span data-stu-id="75327-106">The **New-AzureRmRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="75327-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75327-107">EXAMPLES</span></span>

### <span data-ttu-id="75327-108">Beispiel 1: Erneutes Generieren eines Primärschlüssels</span><span class="sxs-lookup"><span data-stu-id="75327-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="75327-109">Mit diesem Befehl wird der Primärschlüssel eines Zeichenfolgen-Caches neu generiert.</span><span class="sxs-lookup"><span data-stu-id="75327-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="75327-110">Beispiel 2: Erneutes Generieren eines sekundären Schlüssels</span><span class="sxs-lookup"><span data-stu-id="75327-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="75327-111">Mit diesem Befehl wird der sekundäre Schlüssel eines a/a-Caches neu generiert.</span><span class="sxs-lookup"><span data-stu-id="75327-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="75327-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="75327-112">PARAMETERS</span></span>

### <span data-ttu-id="75327-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75327-113">-DefaultProfile</span></span>
<span data-ttu-id="75327-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="75327-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75327-115">-Force</span><span class="sxs-lookup"><span data-stu-id="75327-115">-Force</span></span>
<span data-ttu-id="75327-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="75327-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75327-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="75327-117">-KeyType</span></span>
<span data-ttu-id="75327-118">Gibt an, ob die primäre oder sekundäre Zugriffstaste neu generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="75327-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="75327-119">Gültige Werte sind: primär, sekundär.</span><span class="sxs-lookup"><span data-stu-id="75327-119">Valid values are: Primary, Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75327-120">-Name</span><span class="sxs-lookup"><span data-stu-id="75327-120">-Name</span></span>
<span data-ttu-id="75327-121">Gibt den Namen des Zwischenspeichers mit dem Namenzeichen an.</span><span class="sxs-lookup"><span data-stu-id="75327-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="75327-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75327-122">-ResourceGroupName</span></span>
<span data-ttu-id="75327-123">Gibt den Namen der Ressourcengruppe an, die den Zwischenspeicher mit dem Namenzeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="75327-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="75327-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="75327-124">-Confirm</span></span>
<span data-ttu-id="75327-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="75327-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75327-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75327-126">-WhatIf</span></span>
<span data-ttu-id="75327-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75327-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75327-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75327-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75327-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75327-129">CommonParameters</span></span>
<span data-ttu-id="75327-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75327-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75327-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75327-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75327-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75327-132">INPUTS</span></span>

### <span data-ttu-id="75327-133">System. String</span><span class="sxs-lookup"><span data-stu-id="75327-133">System.String</span></span>

## <span data-ttu-id="75327-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75327-134">OUTPUTS</span></span>

### <span data-ttu-id="75327-135">Microsoft. Azure. Management. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="75327-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="75327-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="75327-136">NOTES</span></span>

## <span data-ttu-id="75327-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75327-137">RELATED LINKS</span></span>

[<span data-ttu-id="75327-138">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="75327-138">Get-AzureRmRedisCacheKey</span></span>](./Get-AzureRmRedisCacheKey.md)


