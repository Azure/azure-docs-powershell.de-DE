---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 541cedecbad563be3e1a016dd651d3e93af44d1e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472663"
---
# <span data-ttu-id="bdc42-101">New-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="bdc42-101">New-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="bdc42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdc42-102">SYNOPSIS</span></span>
<span data-ttu-id="bdc42-103">Erstellt einen Authentifizierungsschlüssel für ein Azure Data Factory-Gateway.</span><span class="sxs-lookup"><span data-stu-id="bdc42-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

## <span data-ttu-id="bdc42-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bdc42-104">SYNTAX</span></span>

### <span data-ttu-id="bdc42-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="bdc42-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdc42-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bdc42-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdc42-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bdc42-107">DESCRIPTION</span></span>
<span data-ttu-id="bdc42-108">Das **Cmdlet "New-AzDataFactoryGatewayAuthKey"** erstellt den Gatewayauthentifizierungsschlüssel für ein angegebenes Azure Data Factory-Gateway.</span><span class="sxs-lookup"><span data-stu-id="bdc42-108">The **New-AzDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="bdc42-109">Mit diesem Schlüssel registrieren Sie das Gateway bei einem Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="bdc42-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="bdc42-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bdc42-110">EXAMPLES</span></span>

### <span data-ttu-id="bdc42-111">Beispiel 1: Erstellen eines Authentifizierungsschlüssels für das Gateway für Schlüssel1</span><span class="sxs-lookup"><span data-stu-id="bdc42-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="bdc42-112">Mit diesem Befehl wird ein Authentifizierungsschlüssel von Schlüssel1 für das Daten factorygateway namens "MyGateway" erstellt.</span><span class="sxs-lookup"><span data-stu-id="bdc42-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="bdc42-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdc42-113">PARAMETERS</span></span>

### <span data-ttu-id="bdc42-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="bdc42-114">-DataFactoryName</span></span>
<span data-ttu-id="bdc42-115">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="bdc42-115">The data factory name.</span></span>

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

### <span data-ttu-id="bdc42-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdc42-116">-DefaultProfile</span></span>
<span data-ttu-id="bdc42-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="bdc42-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdc42-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="bdc42-118">-GatewayName</span></span>
<span data-ttu-id="bdc42-119">Der Name des Daten factorygateways.</span><span class="sxs-lookup"><span data-stu-id="bdc42-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="bdc42-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdc42-120">-InputObject</span></span>
<span data-ttu-id="bdc42-121">Das Data Factory-Objekt</span><span class="sxs-lookup"><span data-stu-id="bdc42-121">The data factory object</span></span>

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

### <span data-ttu-id="bdc42-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="bdc42-122">-KeyName</span></span>
<span data-ttu-id="bdc42-123">Der Name des Gateway-Authentifizierungsschlüssels, der erneut generiert werden soll, entweder "key1" oder "key2".</span><span class="sxs-lookup"><span data-stu-id="bdc42-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdc42-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdc42-124">-ResourceGroupName</span></span>
<span data-ttu-id="bdc42-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bdc42-125">The resource group name.</span></span>

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

### <span data-ttu-id="bdc42-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bdc42-126">-Confirm</span></span>
<span data-ttu-id="bdc42-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bdc42-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdc42-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bdc42-128">-WhatIf</span></span>
<span data-ttu-id="bdc42-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bdc42-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bdc42-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bdc42-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdc42-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdc42-131">CommonParameters</span></span>
<span data-ttu-id="bdc42-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdc42-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdc42-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdc42-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdc42-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bdc42-134">INPUTS</span></span>

### <span data-ttu-id="bdc42-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bdc42-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="bdc42-136">System.String</span><span class="sxs-lookup"><span data-stu-id="bdc42-136">System.String</span></span>

## <span data-ttu-id="bdc42-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bdc42-137">OUTPUTS</span></span>

### <span data-ttu-id="bdc42-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="bdc42-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="bdc42-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bdc42-139">NOTES</span></span>
* <span data-ttu-id="bdc42-140">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="bdc42-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="bdc42-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bdc42-141">RELATED LINKS</span></span>

<span data-ttu-id="bdc42-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="bdc42-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span></span>

