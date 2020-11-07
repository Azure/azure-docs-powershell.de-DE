---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayAuthKey.md
ms.openlocfilehash: b7f435090c0ff5c421df7d8d3e885f67456f9af0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664352"
---
# <span data-ttu-id="323be-101">New-AzureRmDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="323be-101">New-AzureRmDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="323be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="323be-102">SYNOPSIS</span></span>
<span data-ttu-id="323be-103">Erstellt den auth-Schlüssel für ein Azure Data Factory-Gateway.</span><span class="sxs-lookup"><span data-stu-id="323be-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="323be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="323be-104">SYNTAX</span></span>

### <span data-ttu-id="323be-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="323be-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="323be-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="323be-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="323be-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="323be-107">DESCRIPTION</span></span>
<span data-ttu-id="323be-108">Das Cmdlet **New-AzureRmDataFactoryGatewayAuthKey** erstellt Gateway-auth-Schlüssel für ein angegebenes Azure Data Factory-Gateway.</span><span class="sxs-lookup"><span data-stu-id="323be-108">The **New-AzureRmDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="323be-109">Mit diesem Schlüssel registrieren Sie das Gateway bei einem clouddienst.</span><span class="sxs-lookup"><span data-stu-id="323be-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="323be-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="323be-110">EXAMPLES</span></span>

### <span data-ttu-id="323be-111">Beispiel 1: erstellt einen Gateway-auth-Schlüssel für key1</span><span class="sxs-lookup"><span data-stu-id="323be-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzureRmDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="323be-112">Dieser Befehl erstellt einen Gateway-auth-Schlüssel von key1 für das Data Factory-Gateway mit dem Namen mygateway.</span><span class="sxs-lookup"><span data-stu-id="323be-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="323be-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="323be-113">PARAMETERS</span></span>

### <span data-ttu-id="323be-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="323be-114">-DataFactoryName</span></span>
<span data-ttu-id="323be-115">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="323be-115">The data factory name.</span></span>

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

### <span data-ttu-id="323be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="323be-116">-DefaultProfile</span></span>
<span data-ttu-id="323be-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="323be-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="323be-118">-Gatewayname</span><span class="sxs-lookup"><span data-stu-id="323be-118">-GatewayName</span></span>
<span data-ttu-id="323be-119">Der Name des Daten Factory-Gateways.</span><span class="sxs-lookup"><span data-stu-id="323be-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="323be-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="323be-120">-InputObject</span></span>
<span data-ttu-id="323be-121">Das Data Factory-Objekt</span><span class="sxs-lookup"><span data-stu-id="323be-121">The data factory object</span></span>

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

### <span data-ttu-id="323be-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="323be-122">-KeyName</span></span>
<span data-ttu-id="323be-123">Der Name des Gateway-auth-Schlüssels, der neu generiert werden soll, entweder "key1" oder "key2".</span><span class="sxs-lookup"><span data-stu-id="323be-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

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

### <span data-ttu-id="323be-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="323be-124">-ResourceGroupName</span></span>
<span data-ttu-id="323be-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="323be-125">The resource group name.</span></span>

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

### <span data-ttu-id="323be-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="323be-126">-Confirm</span></span>
<span data-ttu-id="323be-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="323be-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="323be-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="323be-128">-WhatIf</span></span>
<span data-ttu-id="323be-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="323be-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="323be-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="323be-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="323be-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="323be-131">CommonParameters</span></span>
<span data-ttu-id="323be-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="323be-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="323be-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="323be-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="323be-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="323be-134">INPUTS</span></span>

### <span data-ttu-id="323be-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="323be-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>
<span data-ttu-id="323be-136">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="323be-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="323be-137">System. String</span><span class="sxs-lookup"><span data-stu-id="323be-137">System.String</span></span>

## <span data-ttu-id="323be-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="323be-138">OUTPUTS</span></span>

### <span data-ttu-id="323be-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="323be-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="323be-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="323be-140">NOTES</span></span>
* <span data-ttu-id="323be-141">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="323be-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="323be-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="323be-142">RELATED LINKS</span></span>

<span data-ttu-id="323be-143">[Neu – AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="323be-143">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)</span></span>

