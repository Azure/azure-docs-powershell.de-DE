---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
ms.openlocfilehash: 1d9b11aa7c259a3534b76a1d1ef011671c7f1142
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950075"
---
# <span data-ttu-id="1a6f6-101">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="1a6f6-101">New-AzRedisCacheKey</span></span>

## <span data-ttu-id="1a6f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a6f6-102">SYNOPSIS</span></span>
<span data-ttu-id="1a6f6-103">Regeneriert den Zugriffsschlüssel eines Redis-Caches.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-103">Regenerates the access key of a Redis Cache.</span></span>

## <span data-ttu-id="1a6f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a6f6-104">SYNTAX</span></span>

```
New-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a6f6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a6f6-105">DESCRIPTION</span></span>
<span data-ttu-id="1a6f6-106">Das **Cmdlet New-AzRedisCacheKey** regeneriert den Zugriffsschlüssel eines Azure Redis Caches.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-106">The **New-AzRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="1a6f6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1a6f6-107">EXAMPLES</span></span>

### <span data-ttu-id="1a6f6-108">Beispiel 1: Neuerieren eines Primärschlüssels</span><span class="sxs-lookup"><span data-stu-id="1a6f6-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="1a6f6-109">Mit diesem Befehl wird der Primärschlüssel eines Redis-Caches neu generiert.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="1a6f6-110">Beispiel 2: Regenerieren eines Sekundärschlüssels</span><span class="sxs-lookup"><span data-stu-id="1a6f6-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="1a6f6-111">Mit diesem Befehl wird der Sekundärschlüssel eines Redis-Caches neu generiert.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="1a6f6-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1a6f6-112">PARAMETERS</span></span>

### <span data-ttu-id="1a6f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a6f6-113">-DefaultProfile</span></span>
<span data-ttu-id="1a6f6-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a6f6-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="1a6f6-115">-Force</span></span>
<span data-ttu-id="1a6f6-116">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1a6f6-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="1a6f6-117">-KeyType</span></span>
<span data-ttu-id="1a6f6-118">Gibt an, ob der primäre oder sekundäre Zugriffsschlüssel neu generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="1a6f6-119">Gültige Werte sind: Primär, Sekundär.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-119">Valid values are: Primary, Secondary.</span></span>

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

### <span data-ttu-id="1a6f6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1a6f6-120">-Name</span></span>
<span data-ttu-id="1a6f6-121">Gibt den Namen des Redis Cache an.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="1a6f6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a6f6-122">-ResourceGroupName</span></span>
<span data-ttu-id="1a6f6-123">Gibt den Namen der Ressourcengruppe an, die den Redis-Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="1a6f6-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1a6f6-124">-Confirm</span></span>
<span data-ttu-id="1a6f6-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a6f6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a6f6-126">-WhatIf</span></span>
<span data-ttu-id="1a6f6-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a6f6-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a6f6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a6f6-129">CommonParameters</span></span>
<span data-ttu-id="1a6f6-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a6f6-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a6f6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a6f6-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1a6f6-132">INPUTS</span></span>

### <span data-ttu-id="1a6f6-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1a6f6-133">System.String</span></span>

## <span data-ttu-id="1a6f6-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1a6f6-134">OUTPUTS</span></span>

### <span data-ttu-id="1a6f6-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="1a6f6-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="1a6f6-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1a6f6-136">NOTES</span></span>

## <span data-ttu-id="1a6f6-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1a6f6-137">RELATED LINKS</span></span>

[<span data-ttu-id="1a6f6-138">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="1a6f6-138">Get-AzRedisCacheKey</span></span>](./Get-AzRedisCacheKey.md)


