---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4DCF54BA-CFFA-4555-8CA3-66B98F704EFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
ms.openlocfilehash: 80d981f4b727d713a5cdc235e9e8ea93d652a358
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651728"
---
# <span data-ttu-id="e6bee-101">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e6bee-101">New-AzDataFactoryGateway</span></span>

## <span data-ttu-id="e6bee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e6bee-102">SYNOPSIS</span></span>
<span data-ttu-id="e6bee-103">Erstellt ein Gateway für eine Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e6bee-103">Creates a gateway for an Azure Data Factory.</span></span>

## <span data-ttu-id="e6bee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6bee-104">SYNTAX</span></span>

### <span data-ttu-id="e6bee-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e6bee-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [[-Description] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6bee-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e6bee-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [[-Description] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6bee-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6bee-107">DESCRIPTION</span></span>
<span data-ttu-id="e6bee-108">Das Cmdlet **New-AzDataFactoryGateway** erstellt ein Gateway in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e6bee-108">The **New-AzDataFactoryGateway** cmdlet creates a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="e6bee-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e6bee-109">EXAMPLES</span></span>

### <span data-ttu-id="e6bee-110">Beispiel 1: Erstellen eines Gateways</span><span class="sxs-lookup"><span data-stu-id="e6bee-110">Example 1: Create a gateway</span></span>
```
PS C:\>New-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name              : ContosoGateway
Description       : my gateway
Version           : 
Status            : NeedRegistration
VersionStatus     : None
CreateTime        : 8/22/2014 1:40:34 AM
RegisterTime      : 
LastConnectTime   : 
ExpiryTime        : 
ProvisioningState : Succeeded
Key               : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

<span data-ttu-id="e6bee-111">Mit diesem Befehl wird ein Gateway mit dem Namen ContosoGateway in der Data Factory mit dem Namen WikiADF in der Ressourcengruppe "ADF" erstellt.</span><span class="sxs-lookup"><span data-stu-id="e6bee-111">This command creates a gateway named ContosoGateway in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="e6bee-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6bee-112">PARAMETERS</span></span>

### <span data-ttu-id="e6bee-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e6bee-113">-DataFactory</span></span>
<span data-ttu-id="e6bee-114">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="e6bee-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="e6bee-115">Dieses Cmdlet erstellt ein Gateway für die Data Factory, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="e6bee-115">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e6bee-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e6bee-116">-DataFactoryName</span></span>
<span data-ttu-id="e6bee-117">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="e6bee-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e6bee-118">Dieses Cmdlet erstellt ein Gateway für die Data Factory, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="e6bee-118">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e6bee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6bee-119">-DefaultProfile</span></span>
<span data-ttu-id="e6bee-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e6bee-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6bee-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6bee-121">-Description</span></span>
<span data-ttu-id="e6bee-122">Gibt eine Beschreibung für das Gateway an.</span><span class="sxs-lookup"><span data-stu-id="e6bee-122">Specifies a description for the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6bee-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e6bee-123">-Name</span></span>
<span data-ttu-id="e6bee-124">Gibt den Namen des zu erstellenden Gateways an.</span><span class="sxs-lookup"><span data-stu-id="e6bee-124">Specifies the name of the gateway to create.</span></span>

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

### <span data-ttu-id="e6bee-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6bee-125">-ResourceGroupName</span></span>
<span data-ttu-id="e6bee-126">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e6bee-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e6bee-127">Mit diesem Cmdlet wird ein Gateway erstellt, das zu der Gruppe gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="e6bee-127">This cmdlet creates a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e6bee-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6bee-128">CommonParameters</span></span>
<span data-ttu-id="e6bee-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6bee-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6bee-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6bee-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6bee-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e6bee-131">INPUTS</span></span>

### <span data-ttu-id="e6bee-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e6bee-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="e6bee-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e6bee-133">System.String</span></span>

## <span data-ttu-id="e6bee-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e6bee-134">OUTPUTS</span></span>

### <span data-ttu-id="e6bee-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e6bee-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="e6bee-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="e6bee-136">NOTES</span></span>
* <span data-ttu-id="e6bee-137">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="e6bee-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e6bee-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e6bee-138">RELATED LINKS</span></span>

[<span data-ttu-id="e6bee-139">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e6bee-139">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="e6bee-140">Satz-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e6bee-140">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


