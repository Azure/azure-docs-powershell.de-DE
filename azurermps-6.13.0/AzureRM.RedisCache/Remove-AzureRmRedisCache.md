---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
ms.openlocfilehash: 35b7d3e05cced593da748f430cb121da43cd0380
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501098"
---
# <span data-ttu-id="9759b-101">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="9759b-101">Remove-AzureRmRedisCache</span></span>

## <span data-ttu-id="9759b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9759b-102">SYNOPSIS</span></span>
<span data-ttu-id="9759b-103">Entfernt einen Zwischenspeicher mit einem Zwischenspeicher.</span><span class="sxs-lookup"><span data-stu-id="9759b-103">Removes a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9759b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9759b-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9759b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9759b-105">DESCRIPTION</span></span>
<span data-ttu-id="9759b-106">Das Cmdlet " **Remove-AzureRmRedisCache** " entfernt einen Azure-a-a-Cache.</span><span class="sxs-lookup"><span data-stu-id="9759b-106">The **Remove-AzureRmRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="9759b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9759b-107">EXAMPLES</span></span>

### <span data-ttu-id="9759b-108">Beispiel 1: Entfernen eines "4-a-Caches" und Zurückgeben des Ergebnisses</span><span class="sxs-lookup"><span data-stu-id="9759b-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="9759b-109">Mit diesem Befehl wird ein a/a-Cache entfernt, und es wird angezeigt, ob der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="9759b-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="9759b-110">Beispiel 2: Entfernen eines Freizeichen folgen-Caches und Anzeigen des Ergebnisses</span><span class="sxs-lookup"><span data-stu-id="9759b-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="9759b-111">Mit diesem Befehl wird ein a/a-Cache entfernt.</span><span class="sxs-lookup"><span data-stu-id="9759b-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="9759b-112">Da der *passthru* -Parameter nicht angegeben wird, wird das Ergebnis des Vorgangs nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9759b-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="9759b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9759b-113">PARAMETERS</span></span>

### <span data-ttu-id="9759b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9759b-114">-DefaultProfile</span></span>
<span data-ttu-id="9759b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9759b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9759b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="9759b-116">-Force</span></span>
<span data-ttu-id="9759b-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="9759b-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9759b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9759b-118">-Name</span></span>
<span data-ttu-id="9759b-119">Gibt den Namen des zu entfernenden zu demontierenden zu löschbaren Speichers</span><span class="sxs-lookup"><span data-stu-id="9759b-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="9759b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9759b-120">-PassThru</span></span>
<span data-ttu-id="9759b-121">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="9759b-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9759b-122">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="9759b-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9759b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9759b-123">-ResourceGroupName</span></span>
<span data-ttu-id="9759b-124">Gibt den Namen der Ressourcengruppe an, die den zu entfernenden zu entfernenden zu entfernenden zu löschenden</span><span class="sxs-lookup"><span data-stu-id="9759b-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="9759b-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9759b-125">-Confirm</span></span>
<span data-ttu-id="9759b-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9759b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9759b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9759b-127">-WhatIf</span></span>
<span data-ttu-id="9759b-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9759b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9759b-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9759b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9759b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9759b-130">CommonParameters</span></span>
<span data-ttu-id="9759b-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9759b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9759b-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9759b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9759b-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9759b-133">INPUTS</span></span>

### <span data-ttu-id="9759b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9759b-134">System.String</span></span>

## <span data-ttu-id="9759b-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9759b-135">OUTPUTS</span></span>

### <span data-ttu-id="9759b-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9759b-136">System.Boolean</span></span>

## <span data-ttu-id="9759b-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="9759b-137">NOTES</span></span>

## <span data-ttu-id="9759b-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9759b-138">RELATED LINKS</span></span>

[<span data-ttu-id="9759b-139">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="9759b-139">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="9759b-140">Neu – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="9759b-140">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="9759b-141">Satz-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="9759b-141">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


