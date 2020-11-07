---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
ms.openlocfilehash: 0f8bd59f6215a2f9cc2bdbcc993da0cb373f70af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820371"
---
# <span data-ttu-id="b1da1-101">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="b1da1-101">Remove-AzDataFactoryGateway</span></span>

## <span data-ttu-id="b1da1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1da1-102">SYNOPSIS</span></span>
<span data-ttu-id="b1da1-103">Entfernt ein Gateway aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b1da1-103">Removes a gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="b1da1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1da1-104">SYNTAX</span></span>

### <span data-ttu-id="b1da1-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b1da1-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1da1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b1da1-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1da1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1da1-107">DESCRIPTION</span></span>
<span data-ttu-id="b1da1-108">Das Cmdlet **Remove-AzDataFactoryGateway** entfernt das angegebene Gateway aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b1da1-108">The **Remove-AzDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="b1da1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1da1-109">EXAMPLES</span></span>

### <span data-ttu-id="b1da1-110">Beispiel 1: Entfernen eines Gateways</span><span class="sxs-lookup"><span data-stu-id="b1da1-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="b1da1-111">Dieser Befehl entfernt das Gateway mit dem Namen ContosoGateway aus der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="b1da1-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="b1da1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1da1-112">PARAMETERS</span></span>

### <span data-ttu-id="b1da1-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b1da1-113">-DataFactory</span></span>
<span data-ttu-id="b1da1-114">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b1da1-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="b1da1-115">Dieses Cmdlet entfernt ein Gateway aus der Data Factory, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b1da1-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b1da1-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="b1da1-116">-DataFactoryName</span></span>
<span data-ttu-id="b1da1-117">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="b1da1-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b1da1-118">Dieses Cmdlet entfernt ein Gateway aus der Data Factory, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b1da1-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b1da1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1da1-119">-DefaultProfile</span></span>
<span data-ttu-id="b1da1-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b1da1-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1da1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b1da1-121">-Force</span></span>
<span data-ttu-id="b1da1-122">Gibt an, dass dieses Cmdlet ein Gateway entfernt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="b1da1-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="b1da1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b1da1-123">-Name</span></span>
<span data-ttu-id="b1da1-124">Gibt den Namen des zu entfernenden Gateways an.</span><span class="sxs-lookup"><span data-stu-id="b1da1-124">Specifies the name of the gateway to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1da1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1da1-125">-ResourceGroupName</span></span>
<span data-ttu-id="b1da1-126">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b1da1-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b1da1-127">Mit diesem Cmdlet wird ein Gateway entfernt, das zu der Gruppe gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b1da1-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b1da1-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b1da1-128">-Confirm</span></span>
<span data-ttu-id="b1da1-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1da1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1da1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1da1-130">-WhatIf</span></span>
<span data-ttu-id="b1da1-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1da1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1da1-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1da1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1da1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1da1-133">CommonParameters</span></span>
<span data-ttu-id="b1da1-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1da1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1da1-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1da1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1da1-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1da1-136">INPUTS</span></span>

### <span data-ttu-id="b1da1-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b1da1-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="b1da1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b1da1-138">System.String</span></span>

## <span data-ttu-id="b1da1-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1da1-139">OUTPUTS</span></span>

### <span data-ttu-id="b1da1-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b1da1-140">System.Boolean</span></span>

## <span data-ttu-id="b1da1-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1da1-141">NOTES</span></span>
* <span data-ttu-id="b1da1-142">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="b1da1-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b1da1-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1da1-143">RELATED LINKS</span></span>

[<span data-ttu-id="b1da1-144">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="b1da1-144">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="b1da1-145">Neu – AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="b1da1-145">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="b1da1-146">Satz-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="b1da1-146">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


