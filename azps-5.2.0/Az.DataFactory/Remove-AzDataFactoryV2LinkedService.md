---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: acd3fadd45dfc32c745af943013f4c0f00b663ad
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298576"
---
# <span data-ttu-id="f84ea-101">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="f84ea-101">Remove-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="f84ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f84ea-102">SYNOPSIS</span></span>
<span data-ttu-id="f84ea-103">Entfernt einen verknüpften Dienst aus Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f84ea-103">Removes a linked service from Data Factory.</span></span>

## <span data-ttu-id="f84ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f84ea-104">SYNTAX</span></span>

### <span data-ttu-id="f84ea-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f84ea-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f84ea-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f84ea-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f84ea-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f84ea-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f84ea-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f84ea-108">DESCRIPTION</span></span>
<span data-ttu-id="f84ea-109">Das Remove-AzDataFactoryV2LinkedService entfernt einen verknüpften Dienst aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f84ea-109">The Remove-AzDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="f84ea-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f84ea-110">EXAMPLES</span></span>

### <span data-ttu-id="f84ea-111">Beispiel 1: Entfernen eines verknüpften Diensts</span><span class="sxs-lookup"><span data-stu-id="f84ea-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="f84ea-112">Mit diesem Befehl wird der verknüpfte Dienst "LinkedServiceTest" aus der Daten factory namens WikiADF entfernt.</span><span class="sxs-lookup"><span data-stu-id="f84ea-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="f84ea-113">Dieser Befehl gibt den Wert "$True" $True.</span><span class="sxs-lookup"><span data-stu-id="f84ea-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="f84ea-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f84ea-114">PARAMETERS</span></span>

### <span data-ttu-id="f84ea-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f84ea-115">-DataFactoryName</span></span>
<span data-ttu-id="f84ea-116">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="f84ea-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f84ea-117">Mit diesem Cmdlet wird ein verknüpfter Dienst aus der von diesem Parameter angegebenen Daten factory entfernt.</span><span class="sxs-lookup"><span data-stu-id="f84ea-117">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f84ea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f84ea-118">-DefaultProfile</span></span>
<span data-ttu-id="f84ea-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f84ea-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f84ea-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f84ea-120">-Force</span></span>
<span data-ttu-id="f84ea-121">Führt das Cmdlet ohne Bestätigungsaufforderung aus.</span><span class="sxs-lookup"><span data-stu-id="f84ea-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f84ea-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f84ea-122">-InputObject</span></span>
<span data-ttu-id="f84ea-123">Gibt das zu entfernende "LinkedService"-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f84ea-123">Specifies the LinkedService object to remove.</span></span>

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

### <span data-ttu-id="f84ea-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f84ea-124">-Name</span></span>
<span data-ttu-id="f84ea-125">Gibt den Namen des verknüpften Diensts an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f84ea-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="f84ea-126">Der Name des verknüpften Diensts.</span><span class="sxs-lookup"><span data-stu-id="f84ea-126">Name of the linked service.</span></span>

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

### <span data-ttu-id="f84ea-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f84ea-127">-ResourceGroupName</span></span>
<span data-ttu-id="f84ea-128">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f84ea-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f84ea-129">Dieses Cmdlet entfernt einen verknüpften Dienst aus der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f84ea-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f84ea-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f84ea-130">-ResourceId</span></span>
<span data-ttu-id="f84ea-131">Die Azure-Ressourcen-ID des verknüpften Diensts, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f84ea-131">The Azure resource ID of the linked service to remove.</span></span>

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

### <span data-ttu-id="f84ea-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f84ea-132">-Confirm</span></span>
<span data-ttu-id="f84ea-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f84ea-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f84ea-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f84ea-134">-WhatIf</span></span>
<span data-ttu-id="f84ea-135">Zeigt, was geschieht, wenn das Cmdlet ausgeführt, aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f84ea-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="f84ea-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f84ea-136">CommonParameters</span></span>
<span data-ttu-id="f84ea-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f84ea-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f84ea-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f84ea-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f84ea-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f84ea-139">INPUTS</span></span>

### <span data-ttu-id="f84ea-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="f84ea-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

### <span data-ttu-id="f84ea-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f84ea-141">System.String</span></span>

## <span data-ttu-id="f84ea-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f84ea-142">OUTPUTS</span></span>

### <span data-ttu-id="f84ea-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="f84ea-143">System.Void</span></span>

## <span data-ttu-id="f84ea-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f84ea-144">NOTES</span></span>
<span data-ttu-id="f84ea-145">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="f84ea-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f84ea-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f84ea-146">RELATED LINKS</span></span>

[<span data-ttu-id="f84ea-147">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="f84ea-147">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="f84ea-148">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="f84ea-148">Set-AzDataFactoryV2LinkedService</span></span>]()

