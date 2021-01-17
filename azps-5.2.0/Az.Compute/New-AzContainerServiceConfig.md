---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
ms.openlocfilehash: a2d55c831860f5664f0f8f3dd5312368a9e5da4d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303955"
---
# <span data-ttu-id="9efb3-101">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="9efb3-101">New-AzContainerServiceConfig</span></span>

## <span data-ttu-id="9efb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9efb3-102">SYNOPSIS</span></span>
<span data-ttu-id="9efb3-103">Erstellt ein lokales Konfigurationsobjekt für einen Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="9efb3-103">Creates a local configuration object for a container service.</span></span>

## <span data-ttu-id="9efb3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9efb3-104">SYNTAX</span></span>

```
New-AzContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9efb3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9efb3-105">DESCRIPTION</span></span>
<span data-ttu-id="9efb3-106">Das **Cmdlet "New-AzContainerServiceConfig"** erstellt ein lokales Konfigurationsobjekt für einen Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="9efb3-106">The **New-AzContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="9efb3-107">Stellen Sie dieses Objekt dem New-AzContainerService cmdlet zum Erstellen eines Containerdiensts zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9efb3-107">Provide this object to the New-AzContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="9efb3-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9efb3-108">EXAMPLES</span></span>

### <span data-ttu-id="9efb3-109">Beispiel 1: Erstellen einer Containerdienstkonfiguration</span><span class="sxs-lookup"><span data-stu-id="9efb3-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="9efb3-110">Dieser Befehl erstellt einen Container und speichert ihn dann in der $Container Variable.</span><span class="sxs-lookup"><span data-stu-id="9efb3-110">This command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="9efb3-111">Der Befehl gibt verschiedene Einstellungen für die Containerdienstkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="9efb3-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="9efb3-112">Der Befehl übergibt das Konfigurationsobjekt mithilfe des Pipelineoperators Add-AzContainerServiceAgentPoolProfile an das Add-AzContainerServiceAgentPoolProfile-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9efb3-112">The command passes the configuration object to the Add-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="9efb3-113">Dieses Cmdlet fügt ein Agentpoolprofil hinzu.</span><span class="sxs-lookup"><span data-stu-id="9efb3-113">That cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="9efb3-114">Geben Sie das Objekt in $Container für den *Parameter "ContainerService"* von **"New-AzContainerService" an.**</span><span class="sxs-lookup"><span data-stu-id="9efb3-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzContainerService**.</span></span>

## <span data-ttu-id="9efb3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9efb3-115">PARAMETERS</span></span>

### <span data-ttu-id="9efb3-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="9efb3-116">-AdminUsername</span></span>
<span data-ttu-id="9efb3-117">Gibt den Administratorkontonamen an, der für einen Linux-basierten Containerdienst verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9efb3-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9efb3-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="9efb3-118">-AgentPoolProfile</span></span>
<span data-ttu-id="9efb3-119">Gibt ein Array von Agentpoolprofilobjekten für den Containerdienst an.</span><span class="sxs-lookup"><span data-stu-id="9efb3-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="9efb3-120">Fügen Sie mithilfe des cmdlets Add-AzContainerServiceAgentPoolProfile ein Profil hinzu.</span><span class="sxs-lookup"><span data-stu-id="9efb3-120">Add a profile by using the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9efb3-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="9efb3-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="9efb3-122">Gibt den benutzerdefinierten Profilsor an.</span><span class="sxs-lookup"><span data-stu-id="9efb3-122">Specifies the custom profile orchestrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9efb3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9efb3-123">-DefaultProfile</span></span>
<span data-ttu-id="9efb3-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9efb3-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9efb3-125">-Location</span><span class="sxs-lookup"><span data-stu-id="9efb3-125">-Location</span></span>
<span data-ttu-id="9efb3-126">Gibt den Speicherort an, an dem der Containerdienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9efb3-126">Specifies the location in which to create the container service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9efb3-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="9efb3-127">-MasterCount</span></span>
<span data-ttu-id="9efb3-128">Gibt die Anzahl der zu erstellenden virtuellen Master computer an.</span><span class="sxs-lookup"><span data-stu-id="9efb3-128">Specifies the number of master virtual machines to create.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9efb3-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="9efb3-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="9efb3-130">Gibt das DNS-Präfix für den virtuellen Mastercomputer an.</span><span class="sxs-lookup"><span data-stu-id="9efb3-130">Specifies the DNS prefix for the master virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9efb3-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="9efb3-131">-OrchestratorType</span></span>
<span data-ttu-id="9efb3-132">Gibt den Typ des Orchestrierens für den Containerdienst an.</span><span class="sxs-lookup"><span data-stu-id="9efb3-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="9efb3-133">Die zulässigen Werte für diesen Parameter sind: DCOS und S vorn.</span><span class="sxs-lookup"><span data-stu-id="9efb3-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Swarm, DCOS, Custom, Kubernetes

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9efb3-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="9efb3-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="9efb3-135">Gibt die Client-ID des Hauptprofils an.</span><span class="sxs-lookup"><span data-stu-id="9efb3-135">Specifies the principal profile client ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9efb3-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="9efb3-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="9efb3-137">Gibt den geheimen Hauptprofilsgeheimnis an.</span><span class="sxs-lookup"><span data-stu-id="9efb3-137">Specifies the principal profile secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9efb3-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="9efb3-138">-SshPublicKey</span></span>
<span data-ttu-id="9efb3-139">Gibt den öffentlichen SSH-Schlüssel für einen Linux-basierten Containerdienst an.</span><span class="sxs-lookup"><span data-stu-id="9efb3-139">Specifies the SSH public key for a Linux-based container service.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9efb3-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="9efb3-140">-Tag</span></span>
<span data-ttu-id="9efb3-141">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="9efb3-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9efb3-142">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="9efb3-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9efb3-143">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="9efb3-143">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="9efb3-144">Gibt an, ob diese Konfiguration die Diagnose für den virtuellen Containerdienstcomputer aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9efb3-144">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9efb3-145">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="9efb3-145">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="9efb3-146">Gibt das Administratorkennwort für einen Containerdienst an, der das Betriebssystem Windows verwendet.</span><span class="sxs-lookup"><span data-stu-id="9efb3-146">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9efb3-147">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="9efb3-147">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="9efb3-148">Gibt den Administratorbenutzernamen für einen Containerdienst an, der das Betriebssystem Windows verwendet.</span><span class="sxs-lookup"><span data-stu-id="9efb3-148">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9efb3-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9efb3-149">-Confirm</span></span>
<span data-ttu-id="9efb3-150">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9efb3-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9efb3-151">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9efb3-151">-WhatIf</span></span>
<span data-ttu-id="9efb3-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9efb3-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9efb3-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9efb3-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9efb3-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9efb3-154">CommonParameters</span></span>
<span data-ttu-id="9efb3-155">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9efb3-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9efb3-156">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9efb3-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9efb3-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9efb3-157">INPUTS</span></span>

### <span data-ttu-id="9efb3-158">System.String</span><span class="sxs-lookup"><span data-stu-id="9efb3-158">System.String</span></span>

### <span data-ttu-id="9efb3-159">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9efb3-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9efb3-160">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="9efb3-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="9efb3-161">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9efb3-161">System.Int32</span></span>

### <span data-ttu-id="9efb3-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span><span class="sxs-lookup"><span data-stu-id="9efb3-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span></span>

### <span data-ttu-id="9efb3-163">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9efb3-163">System.String[]</span></span>

### <span data-ttu-id="9efb3-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9efb3-164">System.Boolean</span></span>

## <span data-ttu-id="9efb3-165">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9efb3-165">OUTPUTS</span></span>

### <span data-ttu-id="9efb3-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="9efb3-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="9efb3-167">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9efb3-167">NOTES</span></span>

## <span data-ttu-id="9efb3-168">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9efb3-168">RELATED LINKS</span></span>

[<span data-ttu-id="9efb3-169">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="9efb3-169">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="9efb3-170">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="9efb3-170">New-AzContainerService</span></span>](./New-AzContainerService.md)
