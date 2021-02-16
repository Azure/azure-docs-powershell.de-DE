---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
ms.openlocfilehash: c396455804f6bb501fa6439fceffb0eb45875516
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148233"
---
# <span data-ttu-id="797b2-101">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="797b2-101">Remove-AzDataFactoryV2</span></span>

## <span data-ttu-id="797b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="797b2-102">SYNOPSIS</span></span>
<span data-ttu-id="797b2-103">Entfernt eine Daten factory.</span><span class="sxs-lookup"><span data-stu-id="797b2-103">Removes a data factory.</span></span>

## <span data-ttu-id="797b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="797b2-104">SYNTAX</span></span>

### <span data-ttu-id="797b2-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="797b2-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="797b2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="797b2-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="797b2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="797b2-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="797b2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="797b2-108">DESCRIPTION</span></span>
<span data-ttu-id="797b2-109">Das Remove-AzDataFactoryV2 cmdlet entfernt eine Daten factory.</span><span class="sxs-lookup"><span data-stu-id="797b2-109">The Remove-AzDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="797b2-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="797b2-110">EXAMPLES</span></span>

### <span data-ttu-id="797b2-111">Beispiel 1: Entfernen einer Daten factory</span><span class="sxs-lookup"><span data-stu-id="797b2-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="797b2-112">Mit diesem Befehl wird die Daten factory namens WikiADF aus der Ressourcengruppe mit dem Namen ADF entfernt.</span><span class="sxs-lookup"><span data-stu-id="797b2-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="797b2-113">Dieser Befehl gibt den Wert "$True" $True.</span><span class="sxs-lookup"><span data-stu-id="797b2-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="797b2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="797b2-114">PARAMETERS</span></span>

### <span data-ttu-id="797b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="797b2-115">-DefaultProfile</span></span>
<span data-ttu-id="797b2-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="797b2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="797b2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="797b2-117">-Force</span></span>
<span data-ttu-id="797b2-118">Führt das Cmdlet ohne Bestätigungsaufforderung aus.</span><span class="sxs-lookup"><span data-stu-id="797b2-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="797b2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="797b2-119">-InputObject</span></span>
<span data-ttu-id="797b2-120">Gibt das zu entfernende "DataFactory"-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="797b2-120">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="797b2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="797b2-121">-Name</span></span>
<span data-ttu-id="797b2-122">Gibt den Namen der zu entfernenden Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="797b2-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797b2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="797b2-123">-ResourceGroupName</span></span>
<span data-ttu-id="797b2-124">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="797b2-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="797b2-125">Dieses Cmdlet entfernt eine Daten factory aus der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="797b2-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797b2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="797b2-126">-ResourceId</span></span>
<span data-ttu-id="797b2-127">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="797b2-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="797b2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="797b2-128">-Confirm</span></span>
<span data-ttu-id="797b2-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="797b2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="797b2-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="797b2-130">-WhatIf</span></span>
<span data-ttu-id="797b2-131">Zeigt, was geschieht, wenn das Cmdlet ausgeführt, aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="797b2-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="797b2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="797b2-132">CommonParameters</span></span>
<span data-ttu-id="797b2-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="797b2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="797b2-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="797b2-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="797b2-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="797b2-135">INPUTS</span></span>

### <span data-ttu-id="797b2-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="797b2-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="797b2-137">System.String</span><span class="sxs-lookup"><span data-stu-id="797b2-137">System.String</span></span>

## <span data-ttu-id="797b2-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="797b2-138">OUTPUTS</span></span>

### <span data-ttu-id="797b2-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="797b2-139">System.Void</span></span>

## <span data-ttu-id="797b2-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="797b2-140">NOTES</span></span>
<span data-ttu-id="797b2-141">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="797b2-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="797b2-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="797b2-142">RELATED LINKS</span></span>

[<span data-ttu-id="797b2-143">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="797b2-143">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="797b2-144">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="797b2-144">Set-AzDataFactoryV2</span></span>]()
