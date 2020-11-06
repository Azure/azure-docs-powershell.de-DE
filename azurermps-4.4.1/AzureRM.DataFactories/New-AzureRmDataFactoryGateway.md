---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 4DCF54BA-CFFA-4555-8CA3-66B98F704EFB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGateway.md
ms.openlocfilehash: 908c2b4804cf242642ce68adf0e28477fae40aac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497105"
---
# <span data-ttu-id="72ae5-101">New-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="72ae5-101">New-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="72ae5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72ae5-102">SYNOPSIS</span></span>
<span data-ttu-id="72ae5-103">Erstellt ein Gateway für eine Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="72ae5-103">Creates a gateway for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72ae5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72ae5-104">SYNTAX</span></span>

### <span data-ttu-id="72ae5-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="72ae5-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [[-Description] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72ae5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="72ae5-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [[-Description] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72ae5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72ae5-107">DESCRIPTION</span></span>
<span data-ttu-id="72ae5-108">Das Cmdlet **New-AzureRmDataFactoryGateway** erstellt ein Gateway in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="72ae5-108">The **New-AzureRmDataFactoryGateway** cmdlet creates a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="72ae5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72ae5-109">EXAMPLES</span></span>

### <span data-ttu-id="72ae5-110">Beispiel 1: Erstellen eines Gateways</span><span class="sxs-lookup"><span data-stu-id="72ae5-110">Example 1: Create a gateway</span></span>
```
PS C:\>New-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
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

<span data-ttu-id="72ae5-111">Mit diesem Befehl wird ein Gateway mit dem Namen ContosoGateway in der Data Factory mit dem Namen WikiADF in der Ressourcengruppe "ADF" erstellt.</span><span class="sxs-lookup"><span data-stu-id="72ae5-111">This command creates a gateway named ContosoGateway in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="72ae5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="72ae5-112">PARAMETERS</span></span>

### <span data-ttu-id="72ae5-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="72ae5-113">-DataFactory</span></span>
<span data-ttu-id="72ae5-114">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="72ae5-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="72ae5-115">Dieses Cmdlet erstellt ein Gateway für die Data Factory, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="72ae5-115">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="72ae5-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="72ae5-116">-DataFactoryName</span></span>
<span data-ttu-id="72ae5-117">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="72ae5-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="72ae5-118">Dieses Cmdlet erstellt ein Gateway für die Data Factory, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="72ae5-118">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="72ae5-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72ae5-119">-Description</span></span>
<span data-ttu-id="72ae5-120">Gibt eine Beschreibung für das Gateway an.</span><span class="sxs-lookup"><span data-stu-id="72ae5-120">Specifies a description for the gateway.</span></span>

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

### <span data-ttu-id="72ae5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="72ae5-121">-Name</span></span>
<span data-ttu-id="72ae5-122">Gibt den Namen des zu erstellenden Gateways an.</span><span class="sxs-lookup"><span data-stu-id="72ae5-122">Specifies the name of the gateway to create.</span></span>

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

### <span data-ttu-id="72ae5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72ae5-123">-ResourceGroupName</span></span>
<span data-ttu-id="72ae5-124">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="72ae5-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="72ae5-125">Mit diesem Cmdlet wird ein Gateway erstellt, das zu der Gruppe gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="72ae5-125">This cmdlet creates a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="72ae5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72ae5-126">-DefaultProfile</span></span>
<span data-ttu-id="72ae5-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="72ae5-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72ae5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72ae5-128">CommonParameters</span></span>
<span data-ttu-id="72ae5-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72ae5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72ae5-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72ae5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72ae5-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72ae5-131">INPUTS</span></span>

## <span data-ttu-id="72ae5-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72ae5-132">OUTPUTS</span></span>

### <span data-ttu-id="72ae5-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="72ae5-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="72ae5-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="72ae5-134">NOTES</span></span>
* <span data-ttu-id="72ae5-135">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="72ae5-135">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="72ae5-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72ae5-136">RELATED LINKS</span></span>

[<span data-ttu-id="72ae5-137">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="72ae5-137">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="72ae5-138">Satz-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="72ae5-138">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


