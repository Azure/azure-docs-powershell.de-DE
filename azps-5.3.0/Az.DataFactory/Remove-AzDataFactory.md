---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
ms.openlocfilehash: 36c22a432d4e281600a1b718c1ac58a851fb7069
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472660"
---
# <span data-ttu-id="1dc02-101">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="1dc02-101">Remove-AzDataFactory</span></span>

## <span data-ttu-id="1dc02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dc02-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc02-103">Entfernt eine Daten factory.</span><span class="sxs-lookup"><span data-stu-id="1dc02-103">Removes a data factory.</span></span>

## <span data-ttu-id="1dc02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1dc02-104">SYNTAX</span></span>

### <span data-ttu-id="1dc02-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="1dc02-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dc02-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1dc02-106">ByFactoryObject</span></span>
```
Remove-AzDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dc02-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1dc02-107">DESCRIPTION</span></span>
<span data-ttu-id="1dc02-108">Das **Cmdlet "Remove-AzDataFactory"** entfernt eine Datenfactory.</span><span class="sxs-lookup"><span data-stu-id="1dc02-108">The **Remove-AzDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="1dc02-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1dc02-109">EXAMPLES</span></span>

### <span data-ttu-id="1dc02-110">Beispiel 1: Entfernen einer Daten factory</span><span class="sxs-lookup"><span data-stu-id="1dc02-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="1dc02-111">Mit diesem Befehl wird die Daten factory namens WikiADF aus der Ressourcengruppe mit dem Namen ADF entfernt.</span><span class="sxs-lookup"><span data-stu-id="1dc02-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="1dc02-112">Dieser Befehl gibt den Wert "$True" $True.</span><span class="sxs-lookup"><span data-stu-id="1dc02-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="1dc02-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1dc02-113">PARAMETERS</span></span>

### <span data-ttu-id="1dc02-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1dc02-114">-DataFactory</span></span>
<span data-ttu-id="1dc02-115">Gibt das **zu entfernende "PSDataFactory"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="1dc02-115">Specifies the **PSDataFactory** object to remove.</span></span>

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

### <span data-ttu-id="1dc02-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc02-116">-DefaultProfile</span></span>
<span data-ttu-id="1dc02-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1dc02-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1dc02-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1dc02-118">-Force</span></span>
<span data-ttu-id="1dc02-119">Gibt an, dass mit diesem Cmdlet eine Daten factory entfernt wird, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="1dc02-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="1dc02-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1dc02-120">-Name</span></span>
<span data-ttu-id="1dc02-121">Gibt den Namen der zu entfernenden Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="1dc02-121">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc02-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dc02-122">-ResourceGroupName</span></span>
<span data-ttu-id="1dc02-123">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1dc02-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1dc02-124">Dieses Cmdlet entfernt eine Daten factory aus der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="1dc02-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1dc02-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1dc02-125">-Confirm</span></span>
<span data-ttu-id="1dc02-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1dc02-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dc02-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1dc02-127">-WhatIf</span></span>
<span data-ttu-id="1dc02-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1dc02-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dc02-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1dc02-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dc02-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc02-130">CommonParameters</span></span>
<span data-ttu-id="1dc02-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dc02-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc02-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dc02-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc02-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1dc02-133">INPUTS</span></span>

### <span data-ttu-id="1dc02-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1dc02-134">System.String</span></span>

### <span data-ttu-id="1dc02-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1dc02-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="1dc02-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1dc02-136">OUTPUTS</span></span>

### <span data-ttu-id="1dc02-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="1dc02-137">System.Void</span></span>

## <span data-ttu-id="1dc02-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1dc02-138">NOTES</span></span>
* <span data-ttu-id="1dc02-139">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="1dc02-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1dc02-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1dc02-140">RELATED LINKS</span></span>

[<span data-ttu-id="1dc02-141">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="1dc02-141">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="1dc02-142">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="1dc02-142">New-AzDataFactory</span></span>](./New-AzDataFactory.md)


