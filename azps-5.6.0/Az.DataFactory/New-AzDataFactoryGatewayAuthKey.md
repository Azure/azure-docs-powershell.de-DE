---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: e58df40aa227e1c8132902c467c2dbcb881c7b6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930096"
---
# <span data-ttu-id="1b9d3-101">New-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="1b9d3-101">New-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="1b9d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b9d3-102">SYNOPSIS</span></span>
<span data-ttu-id="1b9d3-103">Erstellt den Authentifizierungsschlüssel für ein Azure Data Factory Gateway.</span><span class="sxs-lookup"><span data-stu-id="1b9d3-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

## <span data-ttu-id="1b9d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b9d3-104">SYNTAX</span></span>

### <span data-ttu-id="1b9d3-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="1b9d3-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b9d3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1b9d3-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b9d3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b9d3-107">DESCRIPTION</span></span>
<span data-ttu-id="1b9d3-108">Das **Cmdlet New-AzDataFactoryGatewayAuthKey** erstellt den Gateway-Authentifizierungsschlüssel für ein angegebenes Azure Data Factory-Gateway.</span><span class="sxs-lookup"><span data-stu-id="1b9d3-108">The **New-AzDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="1b9d3-109">Sie registrieren das Gateway mit diesem Schlüssel bei einem Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="1b9d3-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="1b9d3-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1b9d3-110">EXAMPLES</span></span>

### <span data-ttu-id="1b9d3-111">Beispiel 1: Erstellt einen Gateway-Authentifizierungsschlüssel für Key1</span><span class="sxs-lookup"><span data-stu-id="1b9d3-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="1b9d3-112">Mit diesem Befehl wird ein Gateway-Authentifizierungsschlüssel von Key1 für das Daten factory-Gateway mit dem Namen MyGateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="1b9d3-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="1b9d3-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1b9d3-113">PARAMETERS</span></span>

### <span data-ttu-id="1b9d3-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1b9d3-114">-DataFactoryName</span></span>
<span data-ttu-id="1b9d3-115">Der Name der Datenfabrik.</span><span class="sxs-lookup"><span data-stu-id="1b9d3-115">The data factory name.</span></span>

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

### <span data-ttu-id="1b9d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b9d3-116">-DefaultProfile</span></span>
<span data-ttu-id="1b9d3-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1b9d3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b9d3-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="1b9d3-118">-GatewayName</span></span>
<span data-ttu-id="1b9d3-119">Der Name des Data Factory-Gateways.</span><span class="sxs-lookup"><span data-stu-id="1b9d3-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="1b9d3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b9d3-120">-InputObject</span></span>
<span data-ttu-id="1b9d3-121">Das Data Factory-Objekt</span><span class="sxs-lookup"><span data-stu-id="1b9d3-121">The data factory object</span></span>

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

### <span data-ttu-id="1b9d3-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="1b9d3-122">-KeyName</span></span>
<span data-ttu-id="1b9d3-123">Der Name des gatewayauth-Schlüssels, der neu generiert werden soll, entweder "key1" oder "key2".</span><span class="sxs-lookup"><span data-stu-id="1b9d3-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

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

### <span data-ttu-id="1b9d3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b9d3-124">-ResourceGroupName</span></span>
<span data-ttu-id="1b9d3-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1b9d3-125">The resource group name.</span></span>

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

### <span data-ttu-id="1b9d3-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1b9d3-126">-Confirm</span></span>
<span data-ttu-id="1b9d3-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1b9d3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b9d3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b9d3-128">-WhatIf</span></span>
<span data-ttu-id="1b9d3-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1b9d3-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b9d3-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b9d3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b9d3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b9d3-131">CommonParameters</span></span>
<span data-ttu-id="1b9d3-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b9d3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b9d3-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b9d3-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b9d3-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1b9d3-134">INPUTS</span></span>

### <span data-ttu-id="1b9d3-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1b9d3-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="1b9d3-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1b9d3-136">System.String</span></span>

## <span data-ttu-id="1b9d3-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1b9d3-137">OUTPUTS</span></span>

### <span data-ttu-id="1b9d3-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="1b9d3-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="1b9d3-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1b9d3-139">NOTES</span></span>
* <span data-ttu-id="1b9d3-140">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="1b9d3-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1b9d3-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1b9d3-141">RELATED LINKS</span></span>

<span data-ttu-id="1b9d3-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="1b9d3-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span></span>

