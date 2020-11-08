---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BED3D3FE-D1E8-4857-A675-7B2670A129B2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 039afbea4d4eb6736cf3b0faebf189edef2d9c26
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006432"
---
# <span data-ttu-id="fed19-101">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fed19-101">New-AzureApplicationGateway</span></span>

## <span data-ttu-id="fed19-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fed19-102">SYNOPSIS</span></span>
<span data-ttu-id="fed19-103">Erstellt ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="fed19-103">Creates an application gateway.</span></span>

## <span data-ttu-id="fed19-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fed19-104">SYNTAX</span></span>

```
New-AzureApplicationGateway -Name <String> -VnetName <String>
 -Subnets <System.Collections.Generic.List`1[System.String]> [-InstanceCount <UInt32>] [-GatewaySize <String>]
 [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fed19-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fed19-105">DESCRIPTION</span></span>
<span data-ttu-id="fed19-106">Das Cmdlet **New-AzureApplicationGateway** erstellt ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="fed19-106">The **New-AzureApplicationGateway** cmdlet creates an application gateway.</span></span>

## <span data-ttu-id="fed19-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fed19-107">EXAMPLES</span></span>

### <span data-ttu-id="fed19-108">Beispiel 1: Erstellen eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="fed19-108">Example 1: Create an application gateway</span></span>
```
PS C:\> New-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork17" -Subnets @("Subnet01", "Subnet02", "Subnet03")
```

<span data-ttu-id="fed19-109">Dieser Befehl erstellt ein Anwendungsgateway mit dem Namen ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="fed19-109">This command creates an application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="fed19-110">Der Befehl stellt das Gateway in VirtualNetwork17 und in den angegebenen Subnetzen bereit.</span><span class="sxs-lookup"><span data-stu-id="fed19-110">The command deploys the gateway in VirtualNetwork17 and in the specified subnets.</span></span>

## <span data-ttu-id="fed19-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="fed19-111">PARAMETERS</span></span>

### <span data-ttu-id="fed19-112">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fed19-112">-Description</span></span>
<span data-ttu-id="fed19-113">Gibt eine Beschreibung an, die dieses Cmdlet dem Anwendungsgateway zuweist.</span><span class="sxs-lookup"><span data-stu-id="fed19-113">Specifies a description that this cmdlet assigns to the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fed19-114">-GatewaySize</span><span class="sxs-lookup"><span data-stu-id="fed19-114">-GatewaySize</span></span>
<span data-ttu-id="fed19-115">Gibt die Größe an, die dieses Cmdlet dem Anwendungsgateway zuweist.</span><span class="sxs-lookup"><span data-stu-id="fed19-115">Specifies the size that this cmdlet assigns to the application gateway.</span></span>
<span data-ttu-id="fed19-116">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="fed19-116">Valid values are:</span></span>

- <span data-ttu-id="fed19-117">Kleine</span><span class="sxs-lookup"><span data-stu-id="fed19-117">Small</span></span>
- <span data-ttu-id="fed19-118">Mittel</span><span class="sxs-lookup"><span data-stu-id="fed19-118">Medium</span></span>
- <span data-ttu-id="fed19-119">Große</span><span class="sxs-lookup"><span data-stu-id="fed19-119">Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fed19-120">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="fed19-120">-InstanceCount</span></span>
<span data-ttu-id="fed19-121">Gibt die Anzahl der Instanzen an, die dieses Cmdlet dem Anwendungsgateway zuweist.</span><span class="sxs-lookup"><span data-stu-id="fed19-121">Specifies the number of instances that this cmdlet assigns to the application gateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fed19-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fed19-122">-Name</span></span>
<span data-ttu-id="fed19-123">Gibt einen Namen für das neue Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="fed19-123">Specifies a name for the new application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fed19-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="fed19-124">-Profile</span></span>
<span data-ttu-id="fed19-125">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="fed19-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fed19-126">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="fed19-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed19-127">-Subnetze</span><span class="sxs-lookup"><span data-stu-id="fed19-127">-Subnets</span></span>
<span data-ttu-id="fed19-128">Gibt ein Array von Subnetzen an, in denen dieses Cmdlet das Anwendungsgateway bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="fed19-128">Specifies an array of subnets in which this cmdlet deploys the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fed19-129">-VnetName</span><span class="sxs-lookup"><span data-stu-id="fed19-129">-VnetName</span></span>
<span data-ttu-id="fed19-130">Gibt das virtuelle Netzwerk an, in dem dieses Cmdlet das Anwendungsgateway bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="fed19-130">Specifies the virtual network in which this cmdlet deploys the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fed19-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fed19-131">CommonParameters</span></span>
<span data-ttu-id="fed19-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fed19-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fed19-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fed19-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fed19-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fed19-134">INPUTS</span></span>

### <span data-ttu-id="fed19-135">System. String</span><span class="sxs-lookup"><span data-stu-id="fed19-135">System.String</span></span>

## <span data-ttu-id="fed19-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fed19-136">OUTPUTS</span></span>

### <span data-ttu-id="fed19-137">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="fed19-137">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="fed19-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="fed19-138">NOTES</span></span>

## <span data-ttu-id="fed19-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fed19-139">RELATED LINKS</span></span>

[<span data-ttu-id="fed19-140">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fed19-140">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="fed19-141">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fed19-141">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="fed19-142">Anfang-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fed19-142">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="fed19-143">Stopp-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fed19-143">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="fed19-144">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fed19-144">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)
