---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
ms.openlocfilehash: b7b01ec1b301741c07a0667931a63287cc503434
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995408"
---
# <span data-ttu-id="be746-101">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="be746-101">Remove-AzFrontDoorContent</span></span>

## <span data-ttu-id="be746-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="be746-102">SYNOPSIS</span></span>
<span data-ttu-id="be746-103">Entfernen von Inhalten in der Haustür</span><span class="sxs-lookup"><span data-stu-id="be746-103">Remove contents in Front Door</span></span>

## <span data-ttu-id="be746-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="be746-104">SYNTAX</span></span>

```
Remove-AzFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be746-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be746-105">DESCRIPTION</span></span>
<span data-ttu-id="be746-106">Remove-AzFrontDoorContent Löscht zwischengespeicherte Inhalte in einer Haustür</span><span class="sxs-lookup"><span data-stu-id="be746-106">Remove-AzFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="be746-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be746-107">EXAMPLES</span></span>

### <span data-ttu-id="be746-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="be746-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="be746-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="be746-109">PARAMETERS</span></span>

### <span data-ttu-id="be746-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="be746-110">-ContentPath</span></span>
<span data-ttu-id="be746-111">Die Pfade zu dem Inhalt, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="be746-111">The paths to the content to be purged.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be746-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be746-112">-DefaultProfile</span></span>
<span data-ttu-id="be746-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="be746-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be746-114">-Name</span><span class="sxs-lookup"><span data-stu-id="be746-114">-Name</span></span>
<span data-ttu-id="be746-115">Name der Haustüre</span><span class="sxs-lookup"><span data-stu-id="be746-115">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be746-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be746-116">-PassThru</span></span>
<span data-ttu-id="be746-117">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="be746-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="be746-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be746-118">-ResourceGroupName</span></span>
<span data-ttu-id="be746-119">Der Ressourcengruppenname der Haustür</span><span class="sxs-lookup"><span data-stu-id="be746-119">The resource group name of the Front Door</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be746-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="be746-120">-Confirm</span></span>
<span data-ttu-id="be746-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="be746-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be746-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be746-122">-WhatIf</span></span>
<span data-ttu-id="be746-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="be746-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be746-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="be746-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be746-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be746-125">CommonParameters</span></span>
<span data-ttu-id="be746-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be746-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be746-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be746-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be746-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="be746-128">INPUTS</span></span>

### <span data-ttu-id="be746-129">Keine</span><span class="sxs-lookup"><span data-stu-id="be746-129">None</span></span>

## <span data-ttu-id="be746-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="be746-130">OUTPUTS</span></span>

### <span data-ttu-id="be746-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="be746-131">System.Boolean</span></span>

## <span data-ttu-id="be746-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="be746-132">NOTES</span></span>

## <span data-ttu-id="be746-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="be746-133">RELATED LINKS</span></span>
