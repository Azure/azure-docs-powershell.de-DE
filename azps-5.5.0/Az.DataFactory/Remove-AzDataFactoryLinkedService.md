---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
ms.openlocfilehash: a8731b075ff5df71aa368fa0c1a3c94ade9ef9e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148236"
---
# <span data-ttu-id="1196d-101">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="1196d-101">Remove-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="1196d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1196d-102">SYNOPSIS</span></span>
<span data-ttu-id="1196d-103">Entfernt einen verknüpften Dienst aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="1196d-103">Removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="1196d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1196d-104">SYNTAX</span></span>

### <span data-ttu-id="1196d-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="1196d-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1196d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1196d-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1196d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1196d-107">DESCRIPTION</span></span>
<span data-ttu-id="1196d-108">Das **Cmdlet "Remove-AzDataFactoryLinkedService"** entfernt einen verknüpften Dienst aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="1196d-108">The **Remove-AzDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="1196d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1196d-109">EXAMPLES</span></span>

### <span data-ttu-id="1196d-110">Beispiel 1: Entfernen eines verknüpften Diensts</span><span class="sxs-lookup"><span data-stu-id="1196d-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="1196d-111">Mit diesem Befehl wird der verknüpfte Dienst "LinkedServiceTest" aus der Daten factory namens WikiADF entfernt.</span><span class="sxs-lookup"><span data-stu-id="1196d-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="1196d-112">Dieser Befehl gibt den Wert "$True" $True.</span><span class="sxs-lookup"><span data-stu-id="1196d-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="1196d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1196d-113">PARAMETERS</span></span>

### <span data-ttu-id="1196d-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1196d-114">-DataFactory</span></span>
<span data-ttu-id="1196d-115">Gibt ein **"PSDataFactory"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="1196d-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="1196d-116">Mit diesem Cmdlet wird ein verknüpfter Dienst aus der von diesem Parameter angegebenen Daten factory entfernt.</span><span class="sxs-lookup"><span data-stu-id="1196d-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1196d-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1196d-117">-DataFactoryName</span></span>
<span data-ttu-id="1196d-118">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="1196d-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1196d-119">Mit diesem Cmdlet wird ein verknüpfter Dienst aus der von diesem Parameter angegebenen Daten factory entfernt.</span><span class="sxs-lookup"><span data-stu-id="1196d-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1196d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1196d-120">-DefaultProfile</span></span>
<span data-ttu-id="1196d-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1196d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1196d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="1196d-122">-Force</span></span>
<span data-ttu-id="1196d-123">Gibt an, dass mit diesem Cmdlet ein verknüpfter Dienst entfernt wird, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="1196d-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="1196d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1196d-124">-Name</span></span>
<span data-ttu-id="1196d-125">Gibt den Namen des verknüpften Diensts an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1196d-125">Specifies the name of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1196d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1196d-126">-ResourceGroupName</span></span>
<span data-ttu-id="1196d-127">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1196d-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1196d-128">Dieses Cmdlet entfernt einen verknüpften Dienst aus der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="1196d-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1196d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1196d-129">-Confirm</span></span>
<span data-ttu-id="1196d-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1196d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1196d-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1196d-131">-WhatIf</span></span>
<span data-ttu-id="1196d-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1196d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1196d-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1196d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1196d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1196d-134">CommonParameters</span></span>
<span data-ttu-id="1196d-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1196d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1196d-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1196d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1196d-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1196d-137">INPUTS</span></span>

### <span data-ttu-id="1196d-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1196d-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="1196d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1196d-139">System.String</span></span>

## <span data-ttu-id="1196d-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1196d-140">OUTPUTS</span></span>

### <span data-ttu-id="1196d-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="1196d-141">System.Void</span></span>

## <span data-ttu-id="1196d-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1196d-142">NOTES</span></span>
* <span data-ttu-id="1196d-143">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="1196d-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1196d-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1196d-144">RELATED LINKS</span></span>

[<span data-ttu-id="1196d-145">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="1196d-145">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="1196d-146">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="1196d-146">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)


