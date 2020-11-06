---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
ms.openlocfilehash: d9ae03325afbfe81c47847cb27df75973221667b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497829"
---
# <span data-ttu-id="be51b-101">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="be51b-101">Remove-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="be51b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="be51b-102">SYNOPSIS</span></span>
<span data-ttu-id="be51b-103">Entfernt ein Gateway aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="be51b-103">Removes a gateway from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be51b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="be51b-104">SYNTAX</span></span>

### <span data-ttu-id="be51b-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="be51b-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be51b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="be51b-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be51b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be51b-107">DESCRIPTION</span></span>
<span data-ttu-id="be51b-108">Das Cmdlet **Remove-AzureRmDataFactoryGateway** entfernt das angegebene Gateway aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="be51b-108">The **Remove-AzureRmDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="be51b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be51b-109">EXAMPLES</span></span>

### <span data-ttu-id="be51b-110">Beispiel 1: Entfernen eines Gateways</span><span class="sxs-lookup"><span data-stu-id="be51b-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzureRmDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="be51b-111">Dieser Befehl entfernt das Gateway mit dem Namen ContosoGateway aus der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="be51b-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="be51b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="be51b-112">PARAMETERS</span></span>

### <span data-ttu-id="be51b-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="be51b-113">-DataFactory</span></span>
<span data-ttu-id="be51b-114">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="be51b-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="be51b-115">Dieses Cmdlet entfernt ein Gateway aus der Data Factory, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="be51b-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="be51b-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="be51b-116">-DataFactoryName</span></span>
<span data-ttu-id="be51b-117">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="be51b-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="be51b-118">Dieses Cmdlet entfernt ein Gateway aus der Data Factory, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="be51b-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="be51b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="be51b-119">-Force</span></span>
<span data-ttu-id="be51b-120">Gibt an, dass dieses Cmdlet ein Gateway entfernt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="be51b-120">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="be51b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="be51b-121">-Name</span></span>
<span data-ttu-id="be51b-122">Gibt den Namen des zu entfernenden Gateways an.</span><span class="sxs-lookup"><span data-stu-id="be51b-122">Specifies the name of the gateway to remove.</span></span>

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

### <span data-ttu-id="be51b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be51b-123">-ResourceGroupName</span></span>
<span data-ttu-id="be51b-124">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="be51b-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="be51b-125">Mit diesem Cmdlet wird ein Gateway entfernt, das zu der Gruppe gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="be51b-125">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="be51b-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="be51b-126">-Confirm</span></span>
<span data-ttu-id="be51b-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="be51b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be51b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be51b-128">-WhatIf</span></span>
<span data-ttu-id="be51b-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="be51b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be51b-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="be51b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be51b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be51b-131">-DefaultProfile</span></span>
<span data-ttu-id="be51b-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="be51b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be51b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be51b-133">CommonParameters</span></span>
<span data-ttu-id="be51b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be51b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be51b-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be51b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be51b-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="be51b-136">INPUTS</span></span>

## <span data-ttu-id="be51b-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="be51b-137">OUTPUTS</span></span>

### <span data-ttu-id="be51b-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="be51b-138">System.Boolean</span></span>

## <span data-ttu-id="be51b-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="be51b-139">NOTES</span></span>
* <span data-ttu-id="be51b-140">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="be51b-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="be51b-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="be51b-141">RELATED LINKS</span></span>

[<span data-ttu-id="be51b-142">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="be51b-142">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="be51b-143">Neu – AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="be51b-143">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="be51b-144">Satz-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="be51b-144">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


