---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
ms.openlocfilehash: 8144d1989f6bec9c1342613cf4776a6dae0a9c27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928643"
---
# <span data-ttu-id="2ff51-101">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="2ff51-101">Remove-AzDataFactoryHub</span></span>

## <span data-ttu-id="2ff51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ff51-102">SYNOPSIS</span></span>
<span data-ttu-id="2ff51-103">Entfernt einen Hub aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="2ff51-103">Removes a hub from Azure Data Factory.</span></span>

## <span data-ttu-id="2ff51-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ff51-104">SYNTAX</span></span>

### <span data-ttu-id="2ff51-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2ff51-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ff51-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2ff51-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ff51-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ff51-107">DESCRIPTION</span></span>
<span data-ttu-id="2ff51-108">Das **Cmdlet Remove-AzDataFactoryHub** entfernt einen Hub aus Azure Data Factory in der angegebenen Azure-Ressourcengruppe und in der angegebenen Daten factory.</span><span class="sxs-lookup"><span data-stu-id="2ff51-108">The **Remove-AzDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="2ff51-109">Wenn Sie einen Hub entfernen, werden auch alle verknüpften Dienste und Pipelines im Hub entfernt.</span><span class="sxs-lookup"><span data-stu-id="2ff51-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="2ff51-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2ff51-110">EXAMPLES</span></span>

### <span data-ttu-id="2ff51-111">Beispiel 1: Entfernen eines Hubs</span><span class="sxs-lookup"><span data-stu-id="2ff51-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="2ff51-112">Mit diesem Befehl wird der Hub mit dem Namen ContosoDataHub aus der Azure-Ressourcengruppe mit dem Namen ADFResourceGroup und der Datenfactory mit dem Namen ADFDataFactory entfernt.</span><span class="sxs-lookup"><span data-stu-id="2ff51-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="2ff51-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2ff51-113">PARAMETERS</span></span>

### <span data-ttu-id="2ff51-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2ff51-114">-DataFactory</span></span>
<span data-ttu-id="2ff51-115">Gibt ein **PSDataFactory-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="2ff51-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="2ff51-116">Dieses Cmdlet entfernt einen Hub aus der Daten factory, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="2ff51-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2ff51-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2ff51-117">-DataFactoryName</span></span>
<span data-ttu-id="2ff51-118">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="2ff51-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="2ff51-119">Dieses Cmdlet entfernt einen Hub aus der Daten factory, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="2ff51-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2ff51-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ff51-120">-DefaultProfile</span></span>
<span data-ttu-id="2ff51-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="2ff51-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ff51-122">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="2ff51-122">-Force</span></span>
<span data-ttu-id="2ff51-123">Gibt an, dass mit diesem Cmdlet ein Hub entfernt wird, ohne Dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="2ff51-123">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="2ff51-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2ff51-124">-Name</span></span>
<span data-ttu-id="2ff51-125">Gibt den Namen des zu entfernenden Hubs an.</span><span class="sxs-lookup"><span data-stu-id="2ff51-125">Specifies the name of the hub to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ff51-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ff51-126">-ResourceGroupName</span></span>
<span data-ttu-id="2ff51-127">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2ff51-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="2ff51-128">Dieses Cmdlet entfernt einen Hub aus der Gruppe, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2ff51-128">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2ff51-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2ff51-129">-Confirm</span></span>
<span data-ttu-id="2ff51-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2ff51-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ff51-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ff51-131">-WhatIf</span></span>
<span data-ttu-id="2ff51-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2ff51-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ff51-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ff51-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ff51-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ff51-134">CommonParameters</span></span>
<span data-ttu-id="2ff51-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ff51-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ff51-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ff51-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ff51-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2ff51-137">INPUTS</span></span>

### <span data-ttu-id="2ff51-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2ff51-138">System.String</span></span>

### <span data-ttu-id="2ff51-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2ff51-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="2ff51-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2ff51-140">OUTPUTS</span></span>

### <span data-ttu-id="2ff51-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2ff51-141">System.Boolean</span></span>

## <span data-ttu-id="2ff51-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2ff51-142">NOTES</span></span>
* <span data-ttu-id="2ff51-143">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="2ff51-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2ff51-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2ff51-144">RELATED LINKS</span></span>

[<span data-ttu-id="2ff51-145">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="2ff51-145">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="2ff51-146">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="2ff51-146">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)


