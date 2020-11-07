---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
ms.openlocfilehash: 1e9895b78bc61155f7cabfc63e6fb5e4cfbcd30d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825139"
---
# <span data-ttu-id="44b36-101">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="44b36-101">Remove-AzRedisCache</span></span>

## <span data-ttu-id="44b36-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="44b36-102">SYNOPSIS</span></span>
<span data-ttu-id="44b36-103">Entfernt einen Zwischenspeicher mit einem Zwischenspeicher.</span><span class="sxs-lookup"><span data-stu-id="44b36-103">Removes a Redis Cache.</span></span>

## <span data-ttu-id="44b36-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="44b36-104">SYNTAX</span></span>

```
Remove-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44b36-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44b36-105">DESCRIPTION</span></span>
<span data-ttu-id="44b36-106">Das Cmdlet " **Remove-AzRedisCache** " entfernt einen Azure-a-a-Cache.</span><span class="sxs-lookup"><span data-stu-id="44b36-106">The **Remove-AzRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="44b36-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44b36-107">EXAMPLES</span></span>

### <span data-ttu-id="44b36-108">Beispiel 1: Entfernen eines "4-a-Caches" und Zurückgeben des Ergebnisses</span><span class="sxs-lookup"><span data-stu-id="44b36-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="44b36-109">Mit diesem Befehl wird ein a/a-Cache entfernt, und es wird angezeigt, ob der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="44b36-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="44b36-110">Beispiel 2: Entfernen eines Freizeichen folgen-Caches und Anzeigen des Ergebnisses</span><span class="sxs-lookup"><span data-stu-id="44b36-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="44b36-111">Mit diesem Befehl wird ein a/a-Cache entfernt.</span><span class="sxs-lookup"><span data-stu-id="44b36-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="44b36-112">Da der *passthru* -Parameter nicht angegeben wird, wird das Ergebnis des Vorgangs nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="44b36-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="44b36-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="44b36-113">PARAMETERS</span></span>

### <span data-ttu-id="44b36-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44b36-114">-DefaultProfile</span></span>
<span data-ttu-id="44b36-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="44b36-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44b36-116">-Force</span><span class="sxs-lookup"><span data-stu-id="44b36-116">-Force</span></span>
<span data-ttu-id="44b36-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="44b36-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="44b36-118">-Name</span><span class="sxs-lookup"><span data-stu-id="44b36-118">-Name</span></span>
<span data-ttu-id="44b36-119">Gibt den Namen des zu entfernenden zu demontierenden zu löschbaren Speichers</span><span class="sxs-lookup"><span data-stu-id="44b36-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="44b36-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44b36-120">-PassThru</span></span>
<span data-ttu-id="44b36-121">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="44b36-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="44b36-122">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="44b36-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="44b36-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44b36-123">-ResourceGroupName</span></span>
<span data-ttu-id="44b36-124">Gibt den Namen der Ressourcengruppe an, die den zu entfernenden zu entfernenden zu entfernenden zu löschenden</span><span class="sxs-lookup"><span data-stu-id="44b36-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="44b36-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="44b36-125">-Confirm</span></span>
<span data-ttu-id="44b36-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="44b36-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44b36-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44b36-127">-WhatIf</span></span>
<span data-ttu-id="44b36-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44b36-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44b36-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="44b36-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44b36-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44b36-130">CommonParameters</span></span>
<span data-ttu-id="44b36-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44b36-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44b36-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44b36-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44b36-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="44b36-133">INPUTS</span></span>

### <span data-ttu-id="44b36-134">System. String</span><span class="sxs-lookup"><span data-stu-id="44b36-134">System.String</span></span>

## <span data-ttu-id="44b36-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="44b36-135">OUTPUTS</span></span>

### <span data-ttu-id="44b36-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="44b36-136">System.Boolean</span></span>

## <span data-ttu-id="44b36-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="44b36-137">NOTES</span></span>

## <span data-ttu-id="44b36-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="44b36-138">RELATED LINKS</span></span>

[<span data-ttu-id="44b36-139">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="44b36-139">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="44b36-140">Neu – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="44b36-140">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="44b36-141">Satz-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="44b36-141">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


