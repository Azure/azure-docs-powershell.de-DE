---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C7F08804-E177-4BC5-8F0E-DEC1B467C4BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20cb37fbba8fd3789c0932f9ff1e9352334662e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006050"
---
# <span data-ttu-id="6ba6a-101">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ba6a-101">Update-AzureApplicationGateway</span></span>

## <span data-ttu-id="6ba6a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6ba6a-102">SYNOPSIS</span></span>
<span data-ttu-id="6ba6a-103">Aktualisiert ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-103">Updates an application gateway.</span></span>

## <span data-ttu-id="6ba6a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ba6a-104">SYNTAX</span></span>

```
Update-AzureApplicationGateway -Name <String> [-VnetName <String>]
 [-Subnets <System.Collections.Generic.List`1[System.String]>] [-InstanceCount <UInt32>]
 [-GatewaySize <String>] [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6ba6a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ba6a-105">DESCRIPTION</span></span>
<span data-ttu-id="6ba6a-106">Das Cmdlet **Update-AzureApplicationGateway** aktualisiert ein vorhandenes Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-106">The **Update-AzureApplicationGateway** cmdlet updates an existing application gateway.</span></span>

## <span data-ttu-id="6ba6a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6ba6a-107">EXAMPLES</span></span>

### <span data-ttu-id="6ba6a-108">Beispiel 1: Ändern eines Anwendungs Gateways mithilfe des Namens</span><span class="sxs-lookup"><span data-stu-id="6ba6a-108">Example 1: Modify an application gateway by using its name</span></span>
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork18" -Subnets @("Subnet05", "Subnet06")
```

<span data-ttu-id="6ba6a-109">Der erste Befehl beendet das Anwendungsgateway mit dem Namen ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-109">The first command stops the application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="6ba6a-110">Ein Anwendungsgateway muss angehalten werden, bevor Sie das virtuelle Netzwerk oder die Subnetze ändern können.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-110">An application gateway must be stopped before you can modify the virtual network or subnets.</span></span>

<span data-ttu-id="6ba6a-111">Der zweite Befehl ändert das virtuelle Subnetz und die Subnetze für das Anwendungsgateway mit dem Namen ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-111">The second command modifies the virtual subnet and subnets for the application gateway named ApplicationGateway06.</span></span>

### <span data-ttu-id="6ba6a-112">Beispiel 2: ändern zusätzlicher Eigenschaften eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="6ba6a-112">Example 2: Modify additional properties of an application gateway</span></span>
```
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -InstanceCount 2 -GatewaySize "Large" -Description "Updated application gateway"
```

<span data-ttu-id="6ba6a-113">Mit diesem Befehl werden die Anzahl der Instanzen, die gatewaygröße und die Beschreibung für das Anwendungsgateway mit dem Namen ApplicationGateway06 geändert.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-113">This command modifies the instance count, gateway size, and description for the application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="6ba6a-114">Mit diesem Befehl werden die virtuellen Netzwerke oder Subnetze für das Anwendungsgateway nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-114">This command does not modify the virtual network or subnets for the application gateway.</span></span>
<span data-ttu-id="6ba6a-115">Daher müssen Sie das Anwendungsgateway nicht beenden, bevor Sie diesen Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-115">Therefore, you do not have to stop the application gateway before you run this command.</span></span>

### <span data-ttu-id="6ba6a-116">Beispiel 3: Ändern eines Anwendungs Gateways mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="6ba6a-116">Example 3: Modify an application gateway by using the pipeline</span></span>
```
PS C:\> $ApplicationGateway = Get-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> $ApplicationGateway.GatewaySize = "Medium"
PS C:\> $ApplicationGateway | Update-AzureApplicationGateway
```

<span data-ttu-id="6ba6a-117">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway06 mit dem Cmdlet **Get-AzureApplicationGateway** ab.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-117">The first command gets the application gateway named ApplicationGateway06 by using the **Get-AzureApplicationGateway** cmdlet.</span></span>
<span data-ttu-id="6ba6a-118">Der Befehl speichert Sie in der $ApplicationGateway-Variablen.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-118">The command stores it in the $ApplicationGateway variable.</span></span>

<span data-ttu-id="6ba6a-119">Der zweite Befehl weist der **GatewaySize** -Eigenschaft den Wert Medium zu.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-119">The second command assigns the **GatewaySize** property the value Medium.</span></span>

<span data-ttu-id="6ba6a-120">Der letzte Befehl übergibt den aktualisierten $ApplicationGateway an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-120">The final command passes the updated $ApplicationGateway to the current cmdlet.</span></span>

## <span data-ttu-id="6ba6a-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ba6a-121">PARAMETERS</span></span>

### <span data-ttu-id="6ba6a-122">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ba6a-122">-Description</span></span>
<span data-ttu-id="6ba6a-123">Gibt eine Beschreibung an, die dieses Cmdlet dem Anwendungsgateway zuweist.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-123">Specifies a description that this cmdlet assigns to the application gateway.</span></span>

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

### <span data-ttu-id="6ba6a-124">-GatewaySize</span><span class="sxs-lookup"><span data-stu-id="6ba6a-124">-GatewaySize</span></span>
<span data-ttu-id="6ba6a-125">Gibt die Größe an, die dieses Cmdlet dem Anwendungsgateway zuweist.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-125">Specifies the size that this cmdlet assigns to the application gateway.</span></span>
<span data-ttu-id="6ba6a-126">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="6ba6a-126">Valid values are:</span></span>

- <span data-ttu-id="6ba6a-127">Kleine</span><span class="sxs-lookup"><span data-stu-id="6ba6a-127">Small</span></span>
- <span data-ttu-id="6ba6a-128">Mittel</span><span class="sxs-lookup"><span data-stu-id="6ba6a-128">Medium</span></span>
- <span data-ttu-id="6ba6a-129">Große</span><span class="sxs-lookup"><span data-stu-id="6ba6a-129">Large</span></span>

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

### <span data-ttu-id="6ba6a-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="6ba6a-130">-InstanceCount</span></span>
<span data-ttu-id="6ba6a-131">Gibt die Anzahl der Instanzen an, die dieses Cmdlet dem Anwendungsgateway zuweist.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-131">Specifies the number of instances that this cmdlet assigns to the application gateway.</span></span>

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

### <span data-ttu-id="6ba6a-132">-Name</span><span class="sxs-lookup"><span data-stu-id="6ba6a-132">-Name</span></span>
<span data-ttu-id="6ba6a-133">Gibt den Namen des Anwendungs Gateways an, das vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-133">Specifies the name of the application gateway that this cmdlet updates.</span></span>

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

### <span data-ttu-id="6ba6a-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="6ba6a-134">-Profile</span></span>
<span data-ttu-id="6ba6a-135">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6ba6a-136">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6ba6a-137">-Subnetze</span><span class="sxs-lookup"><span data-stu-id="6ba6a-137">-Subnets</span></span>
<span data-ttu-id="6ba6a-138">Gibt ein Array von Subnetzen an, in denen dieses Cmdlet das Anwendungsgateway bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-138">Specifies an array of subnets in which this cmdlet deploys the application gateway.</span></span>

<span data-ttu-id="6ba6a-139">Sie können Subnets nicht aktualisieren, während das Anwendungsgateway ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-139">You cannot update subnets while the application gateway is running.</span></span>
<span data-ttu-id="6ba6a-140">Verwenden Sie das Stop-AzureApplicationGateway-Cmdlet, um das Anwendungsgateway zu beenden.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-140">To stop the application gateway, use the Stop-AzureApplicationGateway cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ba6a-141">-VnetName</span><span class="sxs-lookup"><span data-stu-id="6ba6a-141">-VnetName</span></span>
<span data-ttu-id="6ba6a-142">Gibt das virtuelle Netzwerk an, in dem dieses Cmdlet das Anwendungsgateway bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-142">Specifies the virtual network in which this cmdlet deploys the application gateway.</span></span>

<span data-ttu-id="6ba6a-143">Sie können ein virtuelles Netzwerk nicht aktualisieren, während das Anwendungsgateway ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-143">You cannot update a virtual network while the application gateway is running.</span></span>
<span data-ttu-id="6ba6a-144">Verwenden Sie **AzureApplicationGateway** , um das Anwendungsgateway zu beenden.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-144">To stop the application gateway, use **Stop-AzureApplicationGateway**.</span></span>

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

### <span data-ttu-id="6ba6a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ba6a-145">CommonParameters</span></span>
<span data-ttu-id="6ba6a-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ba6a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ba6a-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ba6a-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ba6a-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6ba6a-148">INPUTS</span></span>

### <span data-ttu-id="6ba6a-149">System. String</span><span class="sxs-lookup"><span data-stu-id="6ba6a-149">System.String</span></span>

## <span data-ttu-id="6ba6a-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6ba6a-150">OUTPUTS</span></span>

### <span data-ttu-id="6ba6a-151">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6ba6a-151">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="6ba6a-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="6ba6a-152">NOTES</span></span>

## <span data-ttu-id="6ba6a-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6ba6a-153">RELATED LINKS</span></span>

[<span data-ttu-id="6ba6a-154">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ba6a-154">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="6ba6a-155">Neu – AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ba6a-155">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="6ba6a-156">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ba6a-156">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="6ba6a-157">Anfang-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ba6a-157">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="6ba6a-158">Stopp-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ba6a-158">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)
