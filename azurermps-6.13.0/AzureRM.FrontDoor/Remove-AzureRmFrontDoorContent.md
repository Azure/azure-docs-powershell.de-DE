---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorContent.md
ms.openlocfilehash: c75d8bca528c954cf0612af3392fc79f3cd3b4a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476054"
---
# <span data-ttu-id="95ea5-101">Remove-AzureRmFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="95ea5-101">Remove-AzureRmFrontDoorContent</span></span>

## <span data-ttu-id="95ea5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="95ea5-102">SYNOPSIS</span></span>
<span data-ttu-id="95ea5-103">Entfernen von Inhalten in der Haustür</span><span class="sxs-lookup"><span data-stu-id="95ea5-103">Remove contents in Front Door</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95ea5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="95ea5-104">SYNTAX</span></span>

```
Remove-AzureRmFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95ea5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95ea5-105">DESCRIPTION</span></span>
<span data-ttu-id="95ea5-106">Remove-AzureRmFrontDoorContent Löscht zwischengespeicherte Inhalte in einer Haustür</span><span class="sxs-lookup"><span data-stu-id="95ea5-106">Remove-AzureRmFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="95ea5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="95ea5-107">EXAMPLES</span></span>

### <span data-ttu-id="95ea5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="95ea5-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="95ea5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="95ea5-109">PARAMETERS</span></span>

### <span data-ttu-id="95ea5-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="95ea5-110">-ContentPath</span></span>
<span data-ttu-id="95ea5-111">Die Pfade zu dem Inhalt, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="95ea5-111">The paths to the content to be purged.</span></span>

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

### <span data-ttu-id="95ea5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95ea5-112">-DefaultProfile</span></span>
<span data-ttu-id="95ea5-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="95ea5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95ea5-114">-Name</span><span class="sxs-lookup"><span data-stu-id="95ea5-114">-Name</span></span>
<span data-ttu-id="95ea5-115">Name der Haustüre</span><span class="sxs-lookup"><span data-stu-id="95ea5-115">Front Door name.</span></span>

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

### <span data-ttu-id="95ea5-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95ea5-116">-PassThru</span></span>
<span data-ttu-id="95ea5-117">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="95ea5-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="95ea5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95ea5-118">-ResourceGroupName</span></span>
<span data-ttu-id="95ea5-119">Der Ressourcengruppenname der Haustür</span><span class="sxs-lookup"><span data-stu-id="95ea5-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="95ea5-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="95ea5-120">-Confirm</span></span>
<span data-ttu-id="95ea5-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="95ea5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95ea5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95ea5-122">-WhatIf</span></span>
<span data-ttu-id="95ea5-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="95ea5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95ea5-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95ea5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95ea5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95ea5-125">CommonParameters</span></span>
<span data-ttu-id="95ea5-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95ea5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95ea5-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95ea5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95ea5-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="95ea5-128">INPUTS</span></span>

### <span data-ttu-id="95ea5-129">Keine</span><span class="sxs-lookup"><span data-stu-id="95ea5-129">None</span></span>

## <span data-ttu-id="95ea5-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="95ea5-130">OUTPUTS</span></span>

### <span data-ttu-id="95ea5-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="95ea5-131">System.Boolean</span></span>

## <span data-ttu-id="95ea5-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="95ea5-132">NOTES</span></span>

## <span data-ttu-id="95ea5-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="95ea5-133">RELATED LINKS</span></span>
