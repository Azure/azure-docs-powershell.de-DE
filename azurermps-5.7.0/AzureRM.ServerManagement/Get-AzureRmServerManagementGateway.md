---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: C579BF90-FD8B-4384-96EB-46154E308492
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/get-azurermservermanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
ms.openlocfilehash: 9dc7e38cf169e79ec7dae279c6fa09f069b1ade7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476585"
---
# <span data-ttu-id="88f2f-101">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="88f2f-101">Get-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="88f2f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="88f2f-102">SYNOPSIS</span></span>
<span data-ttu-id="88f2f-103">Ruft mindestens ein Server Verwaltungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="88f2f-103">Gets one or more Server Management Gateways.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88f2f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="88f2f-104">SYNTAX</span></span>

### <span data-ttu-id="88f2f-105">Noparams (Standard)</span><span class="sxs-lookup"><span data-stu-id="88f2f-105">NoParams (Default)</span></span>
```
Get-AzureRmServerManagementGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88f2f-106">Many-ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="88f2f-106">Many-ByResourceGroup</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88f2f-107">Single-ByName</span><span class="sxs-lookup"><span data-stu-id="88f2f-107">Single-ByName</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88f2f-108">Single-ByObject</span><span class="sxs-lookup"><span data-stu-id="88f2f-108">Single-ByObject</span></span>
```
Get-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88f2f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88f2f-109">DESCRIPTION</span></span>
<span data-ttu-id="88f2f-110">Das Cmdlet " **Get-AzureRmServerManagementGateway** " ruft mindestens ein Azure Server Management-Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="88f2f-110">The **Get-AzureRmServerManagementGateway** cmdlet gets one or more Azure Server Management Gateways.</span></span>

## <span data-ttu-id="88f2f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="88f2f-111">EXAMPLES</span></span>

### <span data-ttu-id="88f2f-112">Beispiel 1: Abrufen aller Gateways in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="88f2f-112">Example 1: Get all gateways in a subscription</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
groupOne       centralus      Off          mygateway
groupOne       centralus      Off          othergateway
groupTwo       centralus      On           privategateway
```

<span data-ttu-id="88f2f-113">Dieser Befehl ruft alle Server Verwaltungs Gateways im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="88f2f-113">This command gets all Server Management Gateways in the subscription.</span></span>

### <span data-ttu-id="88f2f-114">Beispiel 2: Abrufen von Gateways in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="88f2f-114">Example 2: Get gateways in a resource group</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway -ResourceGroupName "Group001"
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
myGroup        centralus      Off          mygateway
```

<span data-ttu-id="88f2f-115">Dieser Befehl ruft alle Server Verwaltungs Gateways ab, die zur Ressourcengruppe mit dem Namen Group001 gehören.</span><span class="sxs-lookup"><span data-stu-id="88f2f-115">This command gets all Server Management Gateways that belong to the resource group named Group001.</span></span>

### <span data-ttu-id="88f2f-116">Beispiel 3: Abrufen aller installierten Instanzen eines Gateways</span><span class="sxs-lookup"><span data-stu-id="88f2f-116">Example 3: Get all installed instances of a gateway</span></span>
```
PS C:\>(Get-AzureRmServerManagementGateway -ResourceGroupName "Group002" -GatewayName "Gateway01").Instances
Name             Installed              Version         Operating System
----             ---------              -------         ----------------
GATEWAYPC        4/13/2016 6:35:04 PM   1.0.1104.0      Microsoft Windows 10 Enterprise
```

<span data-ttu-id="88f2f-117">Dieser Befehl ruft alle Instanzen eines Server Verwaltungs Gateways mit dem Namen Gateway01 ab, die zur Ressourcengruppe namens Group002 gehören.</span><span class="sxs-lookup"><span data-stu-id="88f2f-117">This command gets all instances of a Server Management Gateway named Gateway01 that belong to the resource group named Group002.</span></span>

## <span data-ttu-id="88f2f-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="88f2f-118">PARAMETERS</span></span>

### <span data-ttu-id="88f2f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88f2f-119">-DefaultProfile</span></span>
<span data-ttu-id="88f2f-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="88f2f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88f2f-121">-Gateway</span><span class="sxs-lookup"><span data-stu-id="88f2f-121">-Gateway</span></span>
<span data-ttu-id="88f2f-122">Gibt ein Gateway an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="88f2f-122">Specifies a gateway that this cmdlet gets.</span></span>

<span data-ttu-id="88f2f-123">Das Cmdlet verwendet die Parameter *ResourceGroupName* und *GatewayName* über das angegebene Gateway, um die Aktion auszuführen.</span><span class="sxs-lookup"><span data-stu-id="88f2f-123">The cmdlet uses the *ResourceGroupName* and *GatewayName* parameters through the specified Gateway to perform the action.</span></span>

<span data-ttu-id="88f2f-124">Wenn dieser Parameter angegeben wird, enthält dieses Cmdlet den detaillierten Status für das Gateway.</span><span class="sxs-lookup"><span data-stu-id="88f2f-124">When this parameter is specified, this cmdlet will include detailed status for the gateway.</span></span>

```yaml
Type: Gateway
Parameter Sets: Single-ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88f2f-125">-Gatewayname</span><span class="sxs-lookup"><span data-stu-id="88f2f-125">-GatewayName</span></span>
<span data-ttu-id="88f2f-126">Gibt den Namen des Server Verwaltungs Gateways an, für das dieses Cmdlet Gate erhält.</span><span class="sxs-lookup"><span data-stu-id="88f2f-126">Specifies the name of the Server Management Gateway for which this cmdlet gets gate.</span></span>

<span data-ttu-id="88f2f-127">Wenn Sie den Parameter *GatewayName* angeben, enthält dieses Cmdlet den detaillierten Status auf dem Gateway.</span><span class="sxs-lookup"><span data-stu-id="88f2f-127">When you specify the *GatewayName* parameter, this cmdlet will include detailed status on the gateway.</span></span>

```yaml
Type: String
Parameter Sets: Single-ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88f2f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88f2f-128">-ResourceGroupName</span></span>
<span data-ttu-id="88f2f-129">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet Gateways erhält.</span><span class="sxs-lookup"><span data-stu-id="88f2f-129">Specifies the name of the resource group for which this cmdlet gets gateways.</span></span>

```yaml
Type: String
Parameter Sets: Many-ByResourceGroup, Single-ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88f2f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88f2f-130">CommonParameters</span></span>
<span data-ttu-id="88f2f-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88f2f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88f2f-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88f2f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88f2f-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="88f2f-133">INPUTS</span></span>

### <span data-ttu-id="88f2f-134">Gateway</span><span class="sxs-lookup"><span data-stu-id="88f2f-134">Gateway</span></span>
<span data-ttu-id="88f2f-135">Der Parameter "Gateway" akzeptiert den Wert vom Typ "Gateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="88f2f-135">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="88f2f-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="88f2f-136">OUTPUTS</span></span>

### <span data-ttu-id="88f2f-137">Microsoft. Azure. Commands. Servermanagement. Model. Gateway</span><span class="sxs-lookup"><span data-stu-id="88f2f-137">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="88f2f-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="88f2f-138">NOTES</span></span>
* <span data-ttu-id="88f2f-139">Wenn dieses Cmdlet ohne Parameter verwendet wird, gibt es alle Gateways zurück, die dem Abonnement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="88f2f-139">If this cmdlet is use without parameters, it will return all the gateways associated with the subscription.</span></span>

## <span data-ttu-id="88f2f-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="88f2f-140">RELATED LINKS</span></span>

[<span data-ttu-id="88f2f-141">Neu – AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="88f2f-141">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)

[<span data-ttu-id="88f2f-142">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="88f2f-142">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


