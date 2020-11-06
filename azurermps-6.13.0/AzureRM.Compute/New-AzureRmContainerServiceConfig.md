---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
ms.openlocfilehash: 51ebdbffcb88c1d43716170b236332741d05466f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499694"
---
# <span data-ttu-id="d8cfd-101">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="d8cfd-101">New-AzureRmContainerServiceConfig</span></span>

## <span data-ttu-id="d8cfd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d8cfd-102">SYNOPSIS</span></span>
<span data-ttu-id="d8cfd-103">Erstellt ein lokales Konfigurationsobjekt für einen Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-103">Creates a local configuration object for a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8cfd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8cfd-104">SYNTAX</span></span>

```
New-AzureRmContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8cfd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8cfd-105">DESCRIPTION</span></span>
<span data-ttu-id="d8cfd-106">Das Cmdlet **New-AzureRmContainerServiceConfig** erstellt ein lokales Konfigurationsobjekt für einen Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-106">The **New-AzureRmContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="d8cfd-107">Stellen Sie dieses Objekt für das New-AzureRmContainerService-Cmdlet bereit, um einen Containerdienst zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-107">Provide this object to the New-AzureRmContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="d8cfd-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8cfd-108">EXAMPLES</span></span>

### <span data-ttu-id="d8cfd-109">Beispiel 1: Erstellen einer Containerdienst Konfiguration</span><span class="sxs-lookup"><span data-stu-id="d8cfd-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="d8cfd-110">Dieser Befehl erstellt einen Container und speichert ihn dann in der $Container-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-110">This command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="d8cfd-111">Der Befehl gibt verschiedene Einstellungen für die Containerdienst Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="d8cfd-112">Der Befehl übergibt das Konfigurationsobjekt mithilfe des Pipelineoperators an das Add-AzureRmContainerServiceAgentPoolProfile-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-112">The command passes the configuration object to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="d8cfd-113">Mit diesem Cmdlet wird ein Agenten Pool Profil hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-113">That cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="d8cfd-114">Geben Sie das Objekt in $Container für den *ContainerService* -Parameter von **New-AzureRmContainerService** an.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzureRmContainerService**.</span></span>

## <span data-ttu-id="d8cfd-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8cfd-115">PARAMETERS</span></span>

### <span data-ttu-id="d8cfd-116">-Nation aus AdminUsername</span><span class="sxs-lookup"><span data-stu-id="d8cfd-116">-AdminUsername</span></span>
<span data-ttu-id="d8cfd-117">Gibt den Namen des Administratorkontos an, der für einen Linux-basierten Containerdienst verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

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

### <span data-ttu-id="d8cfd-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="d8cfd-118">-AgentPoolProfile</span></span>
<span data-ttu-id="d8cfd-119">Gibt ein Array von Profilobjekten des Agenten Pools für den Containerdienst an.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="d8cfd-120">Fügen Sie mithilfe des Add-AzureRmContainerServiceAgentPoolProfile-Cmdlets ein Profil hinzu.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-120">Add a profile by using the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

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

### <span data-ttu-id="d8cfd-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="d8cfd-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="d8cfd-122">Gibt den benutzerdefinierten Profil-Orchestrator an.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-122">Specifies the custom profile orchestrator.</span></span>

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

### <span data-ttu-id="d8cfd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8cfd-123">-DefaultProfile</span></span>
<span data-ttu-id="d8cfd-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8cfd-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="d8cfd-125">-Location</span></span>
<span data-ttu-id="d8cfd-126">Gibt den Speicherort an, an dem der Containerdienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-126">Specifies the location in which to create the container service.</span></span>

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

### <span data-ttu-id="d8cfd-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="d8cfd-127">-MasterCount</span></span>
<span data-ttu-id="d8cfd-128">Gibt die Anzahl der zu erstellende Master-virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-128">Specifies the number of master virtual machines to create.</span></span>

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

### <span data-ttu-id="d8cfd-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="d8cfd-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="d8cfd-130">Gibt das DNS-Präfix für den virtuellen Mastercomputer an.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-130">Specifies the DNS prefix for the master virtual machine.</span></span>

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

### <span data-ttu-id="d8cfd-131">-Orchestratortype</span><span class="sxs-lookup"><span data-stu-id="d8cfd-131">-OrchestratorType</span></span>
<span data-ttu-id="d8cfd-132">Gibt den Typ des Orchestrators für den Containerdienst an.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="d8cfd-133">Die akzeptablen Werte für diesen Parameter sind: DCOS und Swarm.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

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

### <span data-ttu-id="d8cfd-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="d8cfd-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="d8cfd-135">Gibt die Prinzipal Profil-Client-ID an.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-135">Specifies the principal profile client ID.</span></span>

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

### <span data-ttu-id="d8cfd-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="d8cfd-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="d8cfd-137">Gibt das Hauptprofil Secret an.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-137">Specifies the principal profile secret.</span></span>

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

### <span data-ttu-id="d8cfd-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="d8cfd-138">-SshPublicKey</span></span>
<span data-ttu-id="d8cfd-139">Gibt den öffentlichen SSH-Schlüssel für einen Linux-basierten Containerdienst an.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-139">Specifies the SSH public key for a Linux-based container service.</span></span>

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

### <span data-ttu-id="d8cfd-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="d8cfd-140">-Tag</span></span>
<span data-ttu-id="d8cfd-141">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="d8cfd-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d8cfd-142">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="d8cfd-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d8cfd-143">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="d8cfd-143">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="d8cfd-144">Gibt an, ob diese Konfiguration die Diagnose für den virtuellen Computer des Container Diensts aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-144">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

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

### <span data-ttu-id="d8cfd-145">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="d8cfd-145">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="d8cfd-146">Gibt das Administratorkennwort für einen Containerdienst an, der das Windows-Betriebssystem verwendet.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-146">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="d8cfd-147">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="d8cfd-147">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="d8cfd-148">Gibt den Benutzernamen des Administrators für einen Containerdienst an, der das Windows-Betriebssystem verwendet.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-148">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="d8cfd-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d8cfd-149">-Confirm</span></span>
<span data-ttu-id="d8cfd-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8cfd-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8cfd-151">-WhatIf</span></span>
<span data-ttu-id="d8cfd-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8cfd-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8cfd-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8cfd-154">CommonParameters</span></span>
<span data-ttu-id="d8cfd-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8cfd-156">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8cfd-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8cfd-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d8cfd-157">INPUTS</span></span>

### <span data-ttu-id="d8cfd-158">System. String</span><span class="sxs-lookup"><span data-stu-id="d8cfd-158">System.String</span></span>

### <span data-ttu-id="d8cfd-159">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d8cfd-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d8cfd-160">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. ContainerServiceOrchestratorTypes, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d8cfd-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d8cfd-161">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d8cfd-161">System.Int32</span></span>

### <span data-ttu-id="d8cfd-162">Microsoft. Azure. Management. Compute. Models. ContainerServiceAgentPoolProfile []</span><span class="sxs-lookup"><span data-stu-id="d8cfd-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span></span>

### <span data-ttu-id="d8cfd-163">System. String []</span><span class="sxs-lookup"><span data-stu-id="d8cfd-163">System.String[]</span></span>

### <span data-ttu-id="d8cfd-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d8cfd-164">System.Boolean</span></span>

## <span data-ttu-id="d8cfd-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d8cfd-165">OUTPUTS</span></span>

### <span data-ttu-id="d8cfd-166">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="d8cfd-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="d8cfd-167">Notizen</span><span class="sxs-lookup"><span data-stu-id="d8cfd-167">NOTES</span></span>

## <span data-ttu-id="d8cfd-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d8cfd-168">RELATED LINKS</span></span>

[<span data-ttu-id="d8cfd-169">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="d8cfd-169">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="d8cfd-170">Neu – AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="d8cfd-170">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)
