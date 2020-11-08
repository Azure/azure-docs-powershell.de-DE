---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 8e86597292a9bcfef2163100d273d1e27daeb32a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167235"
---
# <span data-ttu-id="06fb8-101">Get-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="06fb8-101">Get-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="06fb8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="06fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="06fb8-103">Ruft den Gateway-Authentifizierungsschlüssel für eine Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="06fb8-103">Gets gateway auth key for an Azure Data Factory.</span></span>

## <span data-ttu-id="06fb8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="06fb8-104">SYNTAX</span></span>

### <span data-ttu-id="06fb8-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="06fb8-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06fb8-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="06fb8-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06fb8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06fb8-107">DESCRIPTION</span></span>
<span data-ttu-id="06fb8-108">Das Cmdlet " **Get-AzDataFactoryGatewayAuthKey** " Ruft den Gateway-Authentifizierungsschlüssel für ein angegebenes Azure Data Factory-Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="06fb8-108">The **Get-AzDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="06fb8-109">Sie registrieren das Gateway mit einem clouddienst, indem Sie diesen key1 oder key2 dieses auth-Schlüssels verwenden.</span><span class="sxs-lookup"><span data-stu-id="06fb8-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="06fb8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="06fb8-110">EXAMPLES</span></span>

### <span data-ttu-id="06fb8-111">Beispiel 1: Ruft den auth-Schlüssel eines Gateways ab</span><span class="sxs-lookup"><span data-stu-id="06fb8-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="06fb8-112">Dieser Befehl ruft den Gateway-Authentifizierungsschlüssel für das Data Factory-Gateway mit dem Namen mygateway ab.</span><span class="sxs-lookup"><span data-stu-id="06fb8-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="06fb8-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="06fb8-113">PARAMETERS</span></span>

### <span data-ttu-id="06fb8-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="06fb8-114">-DataFactoryName</span></span>
<span data-ttu-id="06fb8-115">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="06fb8-115">The data factory name.</span></span>

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

### <span data-ttu-id="06fb8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06fb8-116">-DefaultProfile</span></span>
<span data-ttu-id="06fb8-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="06fb8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06fb8-118">-Gatewayname</span><span class="sxs-lookup"><span data-stu-id="06fb8-118">-GatewayName</span></span>
<span data-ttu-id="06fb8-119">Der Name des Daten Factory-Gateways.</span><span class="sxs-lookup"><span data-stu-id="06fb8-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="06fb8-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="06fb8-120">-InputObject</span></span>
<span data-ttu-id="06fb8-121">Das Data Factory-Objekt</span><span class="sxs-lookup"><span data-stu-id="06fb8-121">The data factory object</span></span>

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

### <span data-ttu-id="06fb8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06fb8-122">-ResourceGroupName</span></span>
<span data-ttu-id="06fb8-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="06fb8-123">The resource group name.</span></span>

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

### <span data-ttu-id="06fb8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06fb8-124">CommonParameters</span></span>
<span data-ttu-id="06fb8-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06fb8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06fb8-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06fb8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06fb8-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="06fb8-127">INPUTS</span></span>

### <span data-ttu-id="06fb8-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="06fb8-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="06fb8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="06fb8-129">System.String</span></span>

## <span data-ttu-id="06fb8-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="06fb8-130">OUTPUTS</span></span>

### <span data-ttu-id="06fb8-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="06fb8-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="06fb8-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="06fb8-132">NOTES</span></span>
* <span data-ttu-id="06fb8-133">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="06fb8-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="06fb8-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="06fb8-134">RELATED LINKS</span></span>

<span data-ttu-id="06fb8-135">[Neu – AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [Neu – AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="06fb8-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span></span>

