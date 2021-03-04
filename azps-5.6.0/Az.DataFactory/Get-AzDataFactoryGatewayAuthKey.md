---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 7987f014b08250975a2a25323122a081d508b036
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930331"
---
# <span data-ttu-id="38f0b-101">Get-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="38f0b-101">Get-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="38f0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38f0b-102">SYNOPSIS</span></span>
<span data-ttu-id="38f0b-103">Ruft den Gateway-Authentifizierungsschlüssel für eine Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="38f0b-103">Gets gateway auth key for an Azure Data Factory.</span></span>

## <span data-ttu-id="38f0b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38f0b-104">SYNTAX</span></span>

### <span data-ttu-id="38f0b-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="38f0b-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38f0b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="38f0b-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38f0b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38f0b-107">DESCRIPTION</span></span>
<span data-ttu-id="38f0b-108">Das **Get-AzDataFactoryGatewayAuthKey-Cmdlet** ruft den Gateway-Authentifizierungsschlüssel für ein angegebenes Azure Data Factory-Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="38f0b-108">The **Get-AzDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="38f0b-109">Sie registrieren das Gateway bei einem Clouddienst mit diesem Schlüssel1 oder Schlüssel2 dieses Authentifizierungsschlüssels.</span><span class="sxs-lookup"><span data-stu-id="38f0b-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="38f0b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="38f0b-110">EXAMPLES</span></span>

### <span data-ttu-id="38f0b-111">Beispiel 1: Ruft den Authentifizierungsschlüssel eines Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="38f0b-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="38f0b-112">Dieser Befehl ruft den Gateway-Authentifizierungsschlüssel für das Daten factory-Gateway mit dem Namen MyGateway ab.</span><span class="sxs-lookup"><span data-stu-id="38f0b-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="38f0b-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="38f0b-113">PARAMETERS</span></span>

### <span data-ttu-id="38f0b-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="38f0b-114">-DataFactoryName</span></span>
<span data-ttu-id="38f0b-115">Der Name der Datenfabrik.</span><span class="sxs-lookup"><span data-stu-id="38f0b-115">The data factory name.</span></span>

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

### <span data-ttu-id="38f0b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38f0b-116">-DefaultProfile</span></span>
<span data-ttu-id="38f0b-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="38f0b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38f0b-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="38f0b-118">-GatewayName</span></span>
<span data-ttu-id="38f0b-119">Der Name des Data Factory-Gateways.</span><span class="sxs-lookup"><span data-stu-id="38f0b-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="38f0b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38f0b-120">-InputObject</span></span>
<span data-ttu-id="38f0b-121">Das Data Factory-Objekt</span><span class="sxs-lookup"><span data-stu-id="38f0b-121">The data factory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38f0b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38f0b-122">-ResourceGroupName</span></span>
<span data-ttu-id="38f0b-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="38f0b-123">The resource group name.</span></span>

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

### <span data-ttu-id="38f0b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f0b-124">CommonParameters</span></span>
<span data-ttu-id="38f0b-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38f0b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f0b-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38f0b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f0b-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="38f0b-127">INPUTS</span></span>

### <span data-ttu-id="38f0b-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="38f0b-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="38f0b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="38f0b-129">System.String</span></span>

## <span data-ttu-id="38f0b-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="38f0b-130">OUTPUTS</span></span>

### <span data-ttu-id="38f0b-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="38f0b-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="38f0b-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="38f0b-132">NOTES</span></span>
* <span data-ttu-id="38f0b-133">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="38f0b-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="38f0b-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="38f0b-134">RELATED LINKS</span></span>

<span data-ttu-id="38f0b-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="38f0b-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span></span>

