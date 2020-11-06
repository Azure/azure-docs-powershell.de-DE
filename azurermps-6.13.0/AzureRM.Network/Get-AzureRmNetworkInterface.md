---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterface.md
ms.openlocfilehash: e17ac9d538424e3e7883060e6a3dcbec9c6a2c8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505765"
---
# <span data-ttu-id="769fc-101">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="769fc-101">Get-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="769fc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="769fc-102">SYNOPSIS</span></span>
<span data-ttu-id="769fc-103">Ruft eine Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="769fc-103">Gets a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="769fc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="769fc-104">SYNTAX</span></span>

### <span data-ttu-id="769fc-105">NoExpandStandAloneNic (Standard)</span><span class="sxs-lookup"><span data-stu-id="769fc-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="769fc-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="769fc-106">ExpandStandAloneNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="769fc-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="769fc-107">NoExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="769fc-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="769fc-108">ExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="769fc-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="769fc-109">DESCRIPTION</span></span>
<span data-ttu-id="769fc-110">Das Cmdlet " **Get-AzureRmNetworkInterface** " Ruft eine Azure-Netzwerkschnittstelle oder eine Liste von Azure-Netzwerkschnittstellen in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="769fc-110">The **Get-AzureRmNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="769fc-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="769fc-111">EXAMPLES</span></span>

### <span data-ttu-id="769fc-112">Beispiel 1: Abrufen aller Netzwerkschnittstellen</span><span class="sxs-lookup"><span data-stu-id="769fc-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzureRmNetworkInterface
```

<span data-ttu-id="769fc-113">Dieser Befehl ruft alle Netzwerkschnittstellen für das aktuelle Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="769fc-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="769fc-114">Beispiel 2: Abrufen aller Netzwerkschnittstellen mit einem bestimmten Bereitstellungsstatus</span><span class="sxs-lookup"><span data-stu-id="769fc-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="769fc-115">Dieser Befehl ruft alle Netzwerkschnittstellen in der Ressourcengruppe mit dem Namen ResourceGroup1 ab, deren Bereitstellungsstatus "erfolgreich" lautet.</span><span class="sxs-lookup"><span data-stu-id="769fc-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="769fc-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="769fc-116">PARAMETERS</span></span>

### <span data-ttu-id="769fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="769fc-117">-DefaultProfile</span></span>
<span data-ttu-id="769fc-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="769fc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="769fc-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="769fc-119">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="769fc-120">-Name</span><span class="sxs-lookup"><span data-stu-id="769fc-120">-Name</span></span>
<span data-ttu-id="769fc-121">Gibt den Namen der Netzwerkschnittstelle an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="769fc-121">Specifies the name of the network interface that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic, NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="769fc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="769fc-122">-ResourceGroupName</span></span>
<span data-ttu-id="769fc-123">Gibt den Namen der Ressourcengruppe an, aus der dieses Cmdlet Netzwerkschnittstellen erhält.</span><span class="sxs-lookup"><span data-stu-id="769fc-123">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, NoExpandScaleSetNic, ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="769fc-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="769fc-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="769fc-125">Gibt den virtuellen Computer Index des Skalierungs Satzes für virtuelle Maschinen an, von dem dieses Cmdlet Netzwerkschnittstellen erhält.</span><span class="sxs-lookup"><span data-stu-id="769fc-125">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="769fc-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="769fc-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="769fc-127">Gibt den Namen des Skalierungs Satzes für virtuelle Maschinen an, von dem dieses Cmdlet Netzwerkschnittstellen erhält.</span><span class="sxs-lookup"><span data-stu-id="769fc-127">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="769fc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="769fc-128">CommonParameters</span></span>
<span data-ttu-id="769fc-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="769fc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="769fc-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="769fc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="769fc-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="769fc-131">INPUTS</span></span>

### <span data-ttu-id="769fc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="769fc-132">System.String</span></span>

## <span data-ttu-id="769fc-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="769fc-133">OUTPUTS</span></span>

### <span data-ttu-id="769fc-134">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="769fc-134">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="769fc-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="769fc-135">NOTES</span></span>

## <span data-ttu-id="769fc-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="769fc-136">RELATED LINKS</span></span>

[<span data-ttu-id="769fc-137">Neu – AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="769fc-137">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="769fc-138">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="769fc-138">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="769fc-139">Satz-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="769fc-139">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


