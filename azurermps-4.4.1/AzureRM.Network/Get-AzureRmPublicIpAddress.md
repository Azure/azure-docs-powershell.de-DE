---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
ms.openlocfilehash: 9864ba724d20e088e410bc99e8642fae97d71fd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503241"
---
# <span data-ttu-id="739b7-101">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="739b7-101">Get-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="739b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="739b7-102">SYNOPSIS</span></span>
<span data-ttu-id="739b7-103">Ruft eine öffentliche IP-Adresse ab.</span><span class="sxs-lookup"><span data-stu-id="739b7-103">Gets a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="739b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="739b7-104">SYNTAX</span></span>

### <span data-ttu-id="739b7-105">NoExpandStandAloneIp (Standard)</span><span class="sxs-lookup"><span data-stu-id="739b7-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="739b7-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="739b7-106">ExpandStandAloneIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="739b7-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="739b7-107">NoExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="739b7-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="739b7-108">ExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="739b7-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="739b7-109">DESCRIPTION</span></span>
<span data-ttu-id="739b7-110">Das Cmdlet " **Get-AzureRmPublicIPAddress** " ruft mindestens eine öffentliche IP-Adresse in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="739b7-110">The **Get-AzureRmPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="739b7-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="739b7-111">EXAMPLES</span></span>

### <span data-ttu-id="739b7-112">1: Abrufen einer öffentlichen IP-Ressource</span><span class="sxs-lookup"><span data-stu-id="739b7-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="739b7-113">Mit diesem Befehl wird eine öffentliche IP-Adressen Ressource mit dem Namen $publicIPName in der Ressourcengruppe $rgName abgerufen.</span><span class="sxs-lookup"><span data-stu-id="739b7-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="739b7-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="739b7-114">PARAMETERS</span></span>

### <span data-ttu-id="739b7-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="739b7-115">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="739b7-116">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="739b7-116">-IpConfigurationName</span></span>
<span data-ttu-id="739b7-117">IP-Konfigurations Name der Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="739b7-117">Network Interface IP Configuration Name.</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="739b7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="739b7-118">-Name</span></span>
<span data-ttu-id="739b7-119">Gibt den Namen der öffentlichen IP-Adresse an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="739b7-119">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="739b7-120">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="739b7-120">-NetworkInterfaceName</span></span>
<span data-ttu-id="739b7-121">Name der Netzwerkschnittstelle der virtuellen Maschine</span><span class="sxs-lookup"><span data-stu-id="739b7-121">Virtual Machine Network Interface Name.</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="739b7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="739b7-122">-ResourceGroupName</span></span>
<span data-ttu-id="739b7-123">Gibt den Namen der Ressourcengruppe an, die die öffentliche IP-Adresse enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="739b7-123">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="739b7-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="739b7-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="739b7-125">Virtueller Computer-Index.</span><span class="sxs-lookup"><span data-stu-id="739b7-125">Virtual Machine Index.</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="739b7-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="739b7-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="739b7-127">Name des Skalierungs Satzes für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="739b7-127">Virtual Machine Scale Set Name.</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="739b7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="739b7-128">-DefaultProfile</span></span>
<span data-ttu-id="739b7-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="739b7-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="739b7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="739b7-130">CommonParameters</span></span>
<span data-ttu-id="739b7-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="739b7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="739b7-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="739b7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="739b7-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="739b7-133">INPUTS</span></span>

## <span data-ttu-id="739b7-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="739b7-134">OUTPUTS</span></span>

### <span data-ttu-id="739b7-135">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="739b7-135">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="739b7-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="739b7-136">NOTES</span></span>

## <span data-ttu-id="739b7-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="739b7-137">RELATED LINKS</span></span>

[<span data-ttu-id="739b7-138">Neu – AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="739b7-138">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="739b7-139">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="739b7-139">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="739b7-140">Satz-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="739b7-140">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


