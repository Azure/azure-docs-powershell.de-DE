---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: f84973c29d83e8c7c01c3505d17166275a833460
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651693"
---
# <span data-ttu-id="fb8f3-101">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="fb8f3-101">Remove-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="fb8f3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb8f3-102">SYNOPSIS</span></span>
<span data-ttu-id="fb8f3-103">Entfernt einen verknüpften Dienst aus Data Factory.</span><span class="sxs-lookup"><span data-stu-id="fb8f3-103">Removes a linked service from Data Factory.</span></span>

## <span data-ttu-id="fb8f3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb8f3-104">SYNTAX</span></span>

### <span data-ttu-id="fb8f3-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fb8f3-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb8f3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fb8f3-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb8f3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fb8f3-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb8f3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb8f3-108">DESCRIPTION</span></span>
<span data-ttu-id="fb8f3-109">Das Remove-AzDataFactoryV2LinkedService-Cmdlet entfernt einen verknüpften Dienst aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="fb8f3-109">The Remove-AzDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="fb8f3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb8f3-110">EXAMPLES</span></span>

### <span data-ttu-id="fb8f3-111">Beispiel 1: Entfernen eines verknüpften Diensts</span><span class="sxs-lookup"><span data-stu-id="fb8f3-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="fb8f3-112">Mit diesem Befehl wird der verknüpfte Dienst mit dem Namen LinkedServiceTest aus der Data Factory mit dem Namen WikiADF entfernt.</span><span class="sxs-lookup"><span data-stu-id="fb8f3-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="fb8f3-113">Dieser Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="fb8f3-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="fb8f3-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb8f3-114">PARAMETERS</span></span>

### <span data-ttu-id="fb8f3-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="fb8f3-115">-DataFactoryName</span></span>
<span data-ttu-id="fb8f3-116">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="fb8f3-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="fb8f3-117">Mit diesem Cmdlet wird ein verknüpfter Dienst aus der Data Factory entfernt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fb8f3-117">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb8f3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb8f3-118">-DefaultProfile</span></span>
<span data-ttu-id="fb8f3-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fb8f3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb8f3-120">-Force</span><span class="sxs-lookup"><span data-stu-id="fb8f3-120">-Force</span></span>
<span data-ttu-id="fb8f3-121">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="fb8f3-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="fb8f3-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fb8f3-122">-InputObject</span></span>
<span data-ttu-id="fb8f3-123">Gibt das zu entfernende LinkedService-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="fb8f3-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb8f3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="fb8f3-124">-Name</span></span>
<span data-ttu-id="fb8f3-125">Gibt den Namen des zu entfernenden verknüpften Diensts an.</span><span class="sxs-lookup"><span data-stu-id="fb8f3-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="fb8f3-126">Der Name des verknüpften Diensts.</span><span class="sxs-lookup"><span data-stu-id="fb8f3-126">Name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb8f3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb8f3-127">-ResourceGroupName</span></span>
<span data-ttu-id="fb8f3-128">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="fb8f3-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fb8f3-129">Mit diesem Cmdlet wird ein verknüpfter Dienst aus der Gruppe entfernt, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fb8f3-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb8f3-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fb8f3-130">-ResourceId</span></span>
<span data-ttu-id="fb8f3-131">Die Azure-Ressourcen-ID des zu entfernenden verknüpften Diensts.</span><span class="sxs-lookup"><span data-stu-id="fb8f3-131">The Azure resource ID of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb8f3-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fb8f3-132">-Confirm</span></span>
<span data-ttu-id="fb8f3-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fb8f3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb8f3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb8f3-134">-WhatIf</span></span>
<span data-ttu-id="fb8f3-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fb8f3-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="fb8f3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb8f3-136">CommonParameters</span></span>
<span data-ttu-id="fb8f3-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb8f3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb8f3-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb8f3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb8f3-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb8f3-139">INPUTS</span></span>

### <span data-ttu-id="fb8f3-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="fb8f3-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

### <span data-ttu-id="fb8f3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="fb8f3-141">System.String</span></span>

## <span data-ttu-id="fb8f3-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb8f3-142">OUTPUTS</span></span>

### <span data-ttu-id="fb8f3-143">System. void</span><span class="sxs-lookup"><span data-stu-id="fb8f3-143">System.Void</span></span>

## <span data-ttu-id="fb8f3-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb8f3-144">NOTES</span></span>
<span data-ttu-id="fb8f3-145">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="fb8f3-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fb8f3-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb8f3-146">RELATED LINKS</span></span>

[<span data-ttu-id="fb8f3-147">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="fb8f3-147">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="fb8f3-148">Satz-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="fb8f3-148">Set-AzDataFactoryV2LinkedService</span></span>]()

