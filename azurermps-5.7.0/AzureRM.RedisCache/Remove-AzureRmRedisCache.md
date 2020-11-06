---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
ms.openlocfilehash: 4e49fbd2ac2604dab09d79255e7134fee02afd97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482794"
---
# <span data-ttu-id="d901a-101">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d901a-101">Remove-AzureRmRedisCache</span></span>

## <span data-ttu-id="d901a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d901a-102">SYNOPSIS</span></span>
<span data-ttu-id="d901a-103">Entfernt einen Zwischenspeicher mit einem Zwischenspeicher.</span><span class="sxs-lookup"><span data-stu-id="d901a-103">Removes a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d901a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d901a-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d901a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d901a-105">DESCRIPTION</span></span>
<span data-ttu-id="d901a-106">Das Cmdlet " **Remove-AzureRmRedisCache** " entfernt einen Azure-a-a-Cache.</span><span class="sxs-lookup"><span data-stu-id="d901a-106">The **Remove-AzureRmRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="d901a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d901a-107">EXAMPLES</span></span>

### <span data-ttu-id="d901a-108">Beispiel 1: Entfernen eines "4-a-Caches" und Zurückgeben des Ergebnisses</span><span class="sxs-lookup"><span data-stu-id="d901a-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="d901a-109">Mit diesem Befehl wird ein a/a-Cache entfernt, und es wird angezeigt, ob der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="d901a-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="d901a-110">Beispiel 2: Entfernen eines Freizeichen folgen-Caches und Anzeigen des Ergebnisses</span><span class="sxs-lookup"><span data-stu-id="d901a-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="d901a-111">Mit diesem Befehl wird ein a/a-Cache entfernt.</span><span class="sxs-lookup"><span data-stu-id="d901a-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="d901a-112">Da der *passthru* -Parameter nicht angegeben wird, wird das Ergebnis des Vorgangs nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d901a-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="d901a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d901a-113">PARAMETERS</span></span>

### <span data-ttu-id="d901a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d901a-114">-DefaultProfile</span></span>
<span data-ttu-id="d901a-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d901a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d901a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d901a-116">-Force</span></span>
<span data-ttu-id="d901a-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="d901a-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d901a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d901a-118">-Name</span></span>
<span data-ttu-id="d901a-119">Gibt den Namen des zu entfernenden zu demontierenden zu löschbaren Speichers</span><span class="sxs-lookup"><span data-stu-id="d901a-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="d901a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d901a-120">-PassThru</span></span>
<span data-ttu-id="d901a-121">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d901a-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d901a-122">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="d901a-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d901a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d901a-123">-ResourceGroupName</span></span>
<span data-ttu-id="d901a-124">Gibt den Namen der Ressourcengruppe an, die den zu entfernenden zu entfernenden zu entfernenden zu löschenden</span><span class="sxs-lookup"><span data-stu-id="d901a-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="d901a-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d901a-125">-Confirm</span></span>
<span data-ttu-id="d901a-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d901a-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d901a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d901a-127">-WhatIf</span></span>
<span data-ttu-id="d901a-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d901a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d901a-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d901a-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d901a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d901a-130">CommonParameters</span></span>
<span data-ttu-id="d901a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d901a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d901a-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d901a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d901a-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d901a-133">INPUTS</span></span>

### <span data-ttu-id="d901a-134">Keine</span><span class="sxs-lookup"><span data-stu-id="d901a-134">None</span></span>
<span data-ttu-id="d901a-135">Sie können die Eingabe an dieses Cmdlet nach Name, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="d901a-135">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="d901a-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d901a-136">OUTPUTS</span></span>

### <span data-ttu-id="d901a-137">Boolean</span><span class="sxs-lookup"><span data-stu-id="d901a-137">Boolean</span></span>
<span data-ttu-id="d901a-138">Gibt $true zurück, wenn keine Ausnahme eintritt.</span><span class="sxs-lookup"><span data-stu-id="d901a-138">Returns $True if no exception occurs.</span></span>

## <span data-ttu-id="d901a-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="d901a-139">NOTES</span></span>

## <span data-ttu-id="d901a-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d901a-140">RELATED LINKS</span></span>

[<span data-ttu-id="d901a-141">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d901a-141">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="d901a-142">Neu – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d901a-142">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="d901a-143">Satz-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d901a-143">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


