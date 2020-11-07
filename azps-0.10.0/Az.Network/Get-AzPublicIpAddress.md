---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: b9eaacb9a9d779814fc5f0b873aa8e98afedd362
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841531"
---
# <span data-ttu-id="5cede-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5cede-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="5cede-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5cede-102">SYNOPSIS</span></span>
<span data-ttu-id="5cede-103">Ruft eine öffentliche IP-Adresse ab.</span><span class="sxs-lookup"><span data-stu-id="5cede-103">Gets a public IP address.</span></span>

## <span data-ttu-id="5cede-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5cede-104">SYNTAX</span></span>

### <span data-ttu-id="5cede-105">NoExpandStandAloneIp (Standard)</span><span class="sxs-lookup"><span data-stu-id="5cede-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cede-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="5cede-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cede-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="5cede-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cede-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="5cede-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cede-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5cede-109">DESCRIPTION</span></span>
<span data-ttu-id="5cede-110">Das Cmdlet " **Get-AzPublicIPAddress** " ruft mindestens eine öffentliche IP-Adresse in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="5cede-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="5cede-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5cede-111">EXAMPLES</span></span>

### <span data-ttu-id="5cede-112">1: Abrufen einer öffentlichen IP-Ressource</span><span class="sxs-lookup"><span data-stu-id="5cede-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="5cede-113">Mit diesem Befehl wird eine öffentliche IP-Adressen Ressource mit dem Namen $publicIPName in der Ressourcengruppe $rgName abgerufen.</span><span class="sxs-lookup"><span data-stu-id="5cede-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="5cede-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5cede-114">PARAMETERS</span></span>

### <span data-ttu-id="5cede-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cede-115">-DefaultProfile</span></span>
<span data-ttu-id="5cede-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5cede-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cede-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="5cede-117">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cede-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="5cede-118">-IpConfigurationName</span></span>
<span data-ttu-id="5cede-119">IP-Konfigurations Name der Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5cede-119">Network Interface IP Configuration Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cede-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5cede-120">-Name</span></span>
<span data-ttu-id="5cede-121">Gibt den Namen der öffentlichen IP-Adresse an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5cede-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cede-122">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="5cede-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="5cede-123">Name der Netzwerkschnittstelle der virtuellen Maschine</span><span class="sxs-lookup"><span data-stu-id="5cede-123">Virtual Machine Network Interface Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cede-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cede-124">-ResourceGroupName</span></span>
<span data-ttu-id="5cede-125">Gibt den Namen der Ressourcengruppe an, die die öffentliche IP-Adresse enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5cede-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cede-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="5cede-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="5cede-127">Virtueller Computer-Index.</span><span class="sxs-lookup"><span data-stu-id="5cede-127">Virtual Machine Index.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cede-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5cede-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="5cede-129">Name des Skalierungs Satzes für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="5cede-129">Virtual Machine Scale Set Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cede-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cede-130">CommonParameters</span></span>
<span data-ttu-id="5cede-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cede-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cede-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cede-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cede-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5cede-133">INPUTS</span></span>

## <span data-ttu-id="5cede-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5cede-134">OUTPUTS</span></span>

### <span data-ttu-id="5cede-135">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5cede-135">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="5cede-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="5cede-136">NOTES</span></span>

## <span data-ttu-id="5cede-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5cede-137">RELATED LINKS</span></span>

[<span data-ttu-id="5cede-138">Neu – AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5cede-138">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="5cede-139">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5cede-139">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="5cede-140">Satz-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5cede-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


