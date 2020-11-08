---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F8418A93-8E6B-4A1C-B319-7CACE95AB600
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1daf0cb8881beeb71f0b3fe68732d596c56ce12
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006446"
---
# <span data-ttu-id="49e2e-101">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="49e2e-101">Move-AzureService</span></span>

## <span data-ttu-id="49e2e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="49e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="49e2e-103">Migriert einen clouddienst zum Azure Resource Manager-Stapel.</span><span class="sxs-lookup"><span data-stu-id="49e2e-103">Migrates a cloud service to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="49e2e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="49e2e-104">SYNTAX</span></span>

### <span data-ttu-id="49e2e-105">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="49e2e-105">AbortMigrationParameterSet</span></span>
```
Move-AzureService [-Abort] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="49e2e-106">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="49e2e-106">CommitMigrationParameterSet</span></span>
```
Move-AzureService [-Commit] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="49e2e-107">PrepareNewMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="49e2e-107">PrepareNewMigrationParameterSet</span></span>
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="49e2e-108">PrepareExistingMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="49e2e-108">PrepareExistingMigrationParameterSet</span></span>
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="49e2e-109">ValidateNewMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="49e2e-109">ValidateNewMigrationParameterSet</span></span>
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="49e2e-110">ValidateExistingMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="49e2e-110">ValidateExistingMigrationParameterSet</span></span>
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="49e2e-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49e2e-111">DESCRIPTION</span></span>
<span data-ttu-id="49e2e-112">Das Cmdlet **Move-AzureService** migriert einen clouddienst und eine Bereitstellung innerhalb dieses Diensts zu einer Ressourcengruppe im Azure Resource Manager-Stapel.</span><span class="sxs-lookup"><span data-stu-id="49e2e-112">The **Move-AzureService** cmdlet migrates a cloud service and a deployment inside that service to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="49e2e-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49e2e-113">EXAMPLES</span></span>

### <span data-ttu-id="49e2e-114">Beispiel 1: Vorbereiten der Dienst Migration</span><span class="sxs-lookup"><span data-stu-id="49e2e-114">Example 1: Prepare service migration</span></span>
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

<span data-ttu-id="49e2e-115">Dieser Befehl bereitet den Dienst mit dem Namen "ContosoService" für die Migration auf den Azure Resource Manager-Stapel vor.</span><span class="sxs-lookup"><span data-stu-id="49e2e-115">This command prepares the service named ContosoService for migration to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="49e2e-116">Die Migration umfasst die Bereitstellung mit dem Namen ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="49e2e-116">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="49e2e-117">Beispiel 2: Starten der Dienst Migration</span><span class="sxs-lookup"><span data-stu-id="49e2e-117">Example 2: Start service migration</span></span>
```
PS C:\> Move-AzureService -Commit -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

<span data-ttu-id="49e2e-118">Mit diesem Befehl wird die Migration des Diensts mit dem Namen ContosoService zum Azure Resource Manager-Stapel gestartet.</span><span class="sxs-lookup"><span data-stu-id="49e2e-118">This command starts migration of the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="49e2e-119">Die Migration umfasst die Bereitstellung mit dem Namen ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="49e2e-119">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="49e2e-120">Beispiel 3: Abbrechen der Dienst Migration</span><span class="sxs-lookup"><span data-stu-id="49e2e-120">Example 3: Cancel service migration</span></span>
```
PS C:\> Move-AzureService -Abort -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

<span data-ttu-id="49e2e-121">Mit diesem Befehl wird die Migration des Diensts mit dem Namen ContosoService zum Azure Resource Manager-Stapel abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="49e2e-121">This command cancels migration of the service named ContosoService to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="49e2e-122">Beispiel 4: Vorbereiten der Dienst Migration auf ein vorhandenes virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="49e2e-122">Example 4: Prepare service migration to an existing virtual network</span></span>
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "VnetRG" -VirtualNetworkName "ContosoVNET" -SubnetName "ContosoSubnet"
```

<span data-ttu-id="49e2e-123">Dieser Befehl bereitet den Dienst mit dem Namen "ContosoService" für die Migration auf den Azure Resource Manager-Stapel vor.</span><span class="sxs-lookup"><span data-stu-id="49e2e-123">This command prepares the service named ContosoService for migration to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="49e2e-124">Die Migration umfasst die Bereitstellung mit dem Namen ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="49e2e-124">The migration includes the deployment named ContosoVM.</span></span>
<span data-ttu-id="49e2e-125">Bei der Migration wird ein zuvor erstelltes virtuelles Netzwerk verwendet.</span><span class="sxs-lookup"><span data-stu-id="49e2e-125">The migration uses a virtual network that was previously created.</span></span>

### <span data-ttu-id="49e2e-126">Beispiel 5: Überprüfen der Dienst Migration</span><span class="sxs-lookup"><span data-stu-id="49e2e-126">Example 5: Validate service migration</span></span>
```
PS C:\> Move-AzureService -Validate -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

<span data-ttu-id="49e2e-127">Mit diesem Befehl wird die Migration für den Dienst mit dem Namen ContosoService zum Azure Resource Manager-Stapel überprüft.</span><span class="sxs-lookup"><span data-stu-id="49e2e-127">This command validates migration for the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="49e2e-128">Die Migration umfasst die Bereitstellung mit dem Namen ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="49e2e-128">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="49e2e-129">Beispiel 6: Überprüfen der Dienst Migration zu einem vorhandenen virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="49e2e-129">Example 6: Validate service migration to an existing virtual network</span></span>
```
PS C:\> Move-AzureService -Validate -ServiceName "contosoService" -DeploymentName "contosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "vnetRG" -VirtualNetworkName "contosoVNET" -SubnetName "contosoSubnet"
```

<span data-ttu-id="49e2e-130">Mit diesem Befehl wird die Migration für den Dienst mit dem Namen ContosoService zum Azure Resource Manager-Stapel überprüft.</span><span class="sxs-lookup"><span data-stu-id="49e2e-130">This command validates migration for the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="49e2e-131">Die Migration umfasst die Bereitstellung mit dem Namen ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="49e2e-131">The migration includes the deployment named ContosoVM.</span></span>
<span data-ttu-id="49e2e-132">Bei der Migration wird ein zuvor erstelltes virtuelles Netzwerk verwendet.</span><span class="sxs-lookup"><span data-stu-id="49e2e-132">The migration uses a virtual network that was previously created.</span></span>

## <span data-ttu-id="49e2e-133">Parameter</span><span class="sxs-lookup"><span data-stu-id="49e2e-133">PARAMETERS</span></span>

### <span data-ttu-id="49e2e-134">-Abort</span><span class="sxs-lookup"><span data-stu-id="49e2e-134">-Abort</span></span>
<span data-ttu-id="49e2e-135">Gibt an, dass dieses Cmdlet die Dienst Migration abbricht.</span><span class="sxs-lookup"><span data-stu-id="49e2e-135">Indicates that this cmdlet cancels the service migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e2e-136">-Commit</span><span class="sxs-lookup"><span data-stu-id="49e2e-136">-Commit</span></span>
<span data-ttu-id="49e2e-137">Gibt an, dass dieses Cmdlet die Dienst Migration startet.</span><span class="sxs-lookup"><span data-stu-id="49e2e-137">Indicates that this cmdlet starts the service migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e2e-138">-CreateNewVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="49e2e-138">-CreateNewVirtualNetwork</span></span>
<span data-ttu-id="49e2e-139">Gibt an, dass dieses Cmdlet im Azure Resource Manager-Stapel ein virtuelles Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="49e2e-139">Indicates that this cmdlet creates a virtual network in the Azure Resource Manager stack.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, ValidateNewMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e2e-140">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="49e2e-140">-DeploymentName</span></span>
<span data-ttu-id="49e2e-141">Gibt den Namen der Cloud-Dienstbereitstellung an, die dieses Cmdlet migriert.</span><span class="sxs-lookup"><span data-stu-id="49e2e-141">Specifies the name of the cloud service deployment that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e2e-142">-Information</span><span class="sxs-lookup"><span data-stu-id="49e2e-142">-InformationAction</span></span>
<span data-ttu-id="49e2e-143">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="49e2e-143">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="49e2e-144">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="49e2e-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="49e2e-145">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="49e2e-145">Continue</span></span>
- <span data-ttu-id="49e2e-146">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="49e2e-146">Ignore</span></span>
- <span data-ttu-id="49e2e-147">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="49e2e-147">Inquire</span></span>
- <span data-ttu-id="49e2e-148">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="49e2e-148">SilentlyContinue</span></span>
- <span data-ttu-id="49e2e-149">Beenden</span><span class="sxs-lookup"><span data-stu-id="49e2e-149">Stop</span></span>
- <span data-ttu-id="49e2e-150">Anhalten</span><span class="sxs-lookup"><span data-stu-id="49e2e-150">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e2e-151">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="49e2e-151">-InformationVariable</span></span>
<span data-ttu-id="49e2e-152">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="49e2e-152">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e2e-153">-Vorbereiten</span><span class="sxs-lookup"><span data-stu-id="49e2e-153">-Prepare</span></span>
<span data-ttu-id="49e2e-154">Gibt an, dass dieses Cmdlet den cloudbasierten Dienst für die Migration vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="49e2e-154">Indicates that this cmdlet prepares the cloud service for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, PrepareExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e2e-155">-Profil</span><span class="sxs-lookup"><span data-stu-id="49e2e-155">-Profile</span></span>
<span data-ttu-id="49e2e-156">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="49e2e-156">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="49e2e-157">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="49e2e-157">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="49e2e-158">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="49e2e-158">-ServiceName</span></span>
<span data-ttu-id="49e2e-159">Gibt den Namen des Cloud-Diensts an, den dieses Cmdlet migriert.</span><span class="sxs-lookup"><span data-stu-id="49e2e-159">Specifies the name  of the cloud service that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49e2e-160">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="49e2e-160">-SubnetName</span></span>
<span data-ttu-id="49e2e-161">Gibt den Namen des Subnets im virtuellen Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="49e2e-161">Specifies the name of the Subnet inside the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e2e-162">-UseExistingVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="49e2e-162">-UseExistingVirtualNetwork</span></span>
<span data-ttu-id="49e2e-163">Gibt an, dass dieses Cmdlet den cloudbasierten Dienst in ein vorhandenes virtuelles Netzwerk im Azure Resource Manager-Stapel migriert.</span><span class="sxs-lookup"><span data-stu-id="49e2e-163">Indicates that this cmdlet migrates the cloud service to an existing virtual network in the Azure Resource Manager stack.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e2e-164">-Validate</span><span class="sxs-lookup"><span data-stu-id="49e2e-164">-Validate</span></span>
<span data-ttu-id="49e2e-165">Gibt an, dass dieses Cmdlet den cloudbasierten Dienst für die Migration überprüft.</span><span class="sxs-lookup"><span data-stu-id="49e2e-165">Specifies that this cmdlet validates the cloud service for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateNewMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e2e-166">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="49e2e-166">-VirtualNetworkName</span></span>
<span data-ttu-id="49e2e-167">Gibt den Namen eines virtuellen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="49e2e-167">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e2e-168">-VirtualNetworkResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49e2e-168">-VirtualNetworkResourceGroupName</span></span>
<span data-ttu-id="49e2e-169">Gibt den Namen der Ressourcengruppe eines vorhandenen virtuellen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="49e2e-169">Specifies the name of the resource group of an existing virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e2e-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49e2e-170">CommonParameters</span></span>
<span data-ttu-id="49e2e-171">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49e2e-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49e2e-172">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49e2e-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49e2e-173">Eingaben</span><span class="sxs-lookup"><span data-stu-id="49e2e-173">INPUTS</span></span>

## <span data-ttu-id="49e2e-174">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49e2e-174">OUTPUTS</span></span>

## <span data-ttu-id="49e2e-175">Notizen</span><span class="sxs-lookup"><span data-stu-id="49e2e-175">NOTES</span></span>

## <span data-ttu-id="49e2e-176">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="49e2e-176">RELATED LINKS</span></span>

[<span data-ttu-id="49e2e-177">Verschieben-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="49e2e-177">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="49e2e-178">Verschieben-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="49e2e-178">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="49e2e-179">Verschieben-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="49e2e-179">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="49e2e-180">Verschieben-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="49e2e-180">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="49e2e-181">Verschieben-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="49e2e-181">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


