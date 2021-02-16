---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
ms.openlocfilehash: 2821e9404fe4101415aa04a8b0d331b3066563df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144708"
---
# <span data-ttu-id="893eb-101">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="893eb-101">Set-AzVMChefExtension</span></span>

## <span data-ttu-id="893eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="893eb-102">SYNOPSIS</span></span>
<span data-ttu-id="893eb-103">Fügt einem virtuellen Computer eine "Chef"-Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="893eb-103">Adds a Chef extension to a virtual machine.</span></span>

## <span data-ttu-id="893eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="893eb-104">SYNTAX</span></span>

### <span data-ttu-id="893eb-105">Linux</span><span class="sxs-lookup"><span data-stu-id="893eb-105">Linux</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="893eb-106">Windows</span><span class="sxs-lookup"><span data-stu-id="893eb-106">Windows</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="893eb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="893eb-107">DESCRIPTION</span></span>
<span data-ttu-id="893eb-108">Das **Cmdlet "Set-AzVM VirtualExtension"** fügt dem virtuellen Computer die Erweiterung "Chef" hinzu.</span><span class="sxs-lookup"><span data-stu-id="893eb-108">The **Set-AzVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="893eb-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="893eb-109">EXAMPLES</span></span>

### <span data-ttu-id="893eb-110">Beispiel 1: Hinzufügen einer Erweiterung "Chef" zu einem virtuellen Windows-Computer</span><span class="sxs-lookup"><span data-stu-id="893eb-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="893eb-111">Dieser Befehl fügt einem virtuellen Windows-Computer mit dem Namen "WindowsVM001" eine "Chef"-Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="893eb-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="893eb-112">Wenn der virtuelle Computer gestartet wird, bootstrapst Chef den virtuellen Computer, um Apache ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="893eb-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="893eb-113">Beispiel 2: Hinzufügen einer Erweiterung "Chef" zu einem virtuellen Linux-Computer</span><span class="sxs-lookup"><span data-stu-id="893eb-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="893eb-114">Dieser Befehl fügt einem virtuellen Linux-Computer namens LinuxVM001 eine "Chef"-Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="893eb-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="893eb-115">Wenn der virtuelle Computer gestartet wird, bootstrapst Chef den virtuellen Computer, um Apache ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="893eb-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="893eb-116">Beispiel 3: Hinzufügen einer Erweiterung "Chef" zu einem virtuellen Windows-Computer mit Bootstrapoptionen</span><span class="sxs-lookup"><span data-stu-id="893eb-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="893eb-117">Mit diesem Befehl wird die Erweiterung "Chef" einem virtuellen Windows-Computer namens "WindowsVM002" hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="893eb-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="893eb-118">Wenn der virtuelle Computer gestartet wird, bootstrapst Chef den virtuellen Computer, um Apache ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="893eb-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="893eb-119">Nach dem Bootstrapping verweist der virtuelle Computer auf die BootstrapOptions, die im JSON-Format angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="893eb-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="893eb-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="893eb-120">PARAMETERS</span></span>

### <span data-ttu-id="893eb-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="893eb-121">-AutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="893eb-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="893eb-122">-BootstrapOptions</span></span>
<span data-ttu-id="893eb-123">Gibt die Konfigurationseinstellungen in der Option client_rb an.</span><span class="sxs-lookup"><span data-stu-id="893eb-123">Specifies configuration settings in the client_rb option.</span></span>

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

### <span data-ttu-id="893eb-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="893eb-124">-BootstrapVersion</span></span>
<span data-ttu-id="893eb-125">Gibt die Version der Bootstrapkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="893eb-125">Specifies the version of the bootstrap configuration.</span></span>

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

### <span data-ttu-id="893eb-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="893eb-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="893eb-127">Gibt die Häufigkeit (in Minuten) an, mit der der Chefservice ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="893eb-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="893eb-128">Wenn Sie nicht möchten, dass der Chefdienst auf der Azure VM installiert wird, legen Sie in diesem Feld den Wert "0" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="893eb-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="893eb-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="893eb-129">-ChefServerUrl</span></span>
<span data-ttu-id="893eb-130">Gibt den Chefserverlink als URL an.</span><span class="sxs-lookup"><span data-stu-id="893eb-130">Specifies the Chef server link, as a URL.</span></span>

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

### <span data-ttu-id="893eb-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="893eb-131">-ClientRb</span></span>
<span data-ttu-id="893eb-132">Gibt den vollständigen Pfad von "Chef client.rb" an.</span><span class="sxs-lookup"><span data-stu-id="893eb-132">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="893eb-133">-Thread</span><span class="sxs-lookup"><span data-stu-id="893eb-133">-Daemon</span></span>
<span data-ttu-id="893eb-134">Konfiguriert den Chef-Client-Dienst für die unbeaufsichtigte Ausführung.</span><span class="sxs-lookup"><span data-stu-id="893eb-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="893eb-135">Die Knotenplattform sollte Windows sein.</span><span class="sxs-lookup"><span data-stu-id="893eb-135">The node platform should be Windows.</span></span>
<span data-ttu-id="893eb-136">Zulässige Optionen: "keine", "Dienst" und "Aufgabe".</span><span class="sxs-lookup"><span data-stu-id="893eb-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="893eb-137">none – Zurzeit wird verhindert, dass der Chef-Client-Dienst als Dienst konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="893eb-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="893eb-138">Service – Konfiguriert den Chef-Client so, dass er automatisch im Hintergrund als Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="893eb-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="893eb-139">task – Konfiguriert den Chef-Client so, dass er automatisch als geplante Aufgabe im Hintergrund ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="893eb-139">task - Configures the chef-client to run automatically in the background as a scheduled task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: none, service, task

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="893eb-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="893eb-140">-DefaultProfile</span></span>
<span data-ttu-id="893eb-141">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="893eb-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="893eb-142">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="893eb-142">-JsonAttribute</span></span>
<span data-ttu-id="893eb-143">Eine JSON-Zeichenfolge, die der ersten Ausführung von "chef-client" hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="893eb-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="893eb-144">z. B. -JsonAttribute '{"foo" : "bar"}'</span><span class="sxs-lookup"><span data-stu-id="893eb-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="893eb-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="893eb-145">-Linux</span></span>
<span data-ttu-id="893eb-146">Gibt an, dass mit diesem Cmdlet ein virtueller Windows-Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="893eb-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893eb-147">-Location</span><span class="sxs-lookup"><span data-stu-id="893eb-147">-Location</span></span>
<span data-ttu-id="893eb-148">Gibt den Speicherort des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="893eb-148">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="893eb-149">-Name</span><span class="sxs-lookup"><span data-stu-id="893eb-149">-Name</span></span>
<span data-ttu-id="893eb-150">Gibt den Namen der Erweiterung "Chef" an.</span><span class="sxs-lookup"><span data-stu-id="893eb-150">Specifies the name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="893eb-151">-NoWait</span><span class="sxs-lookup"><span data-stu-id="893eb-151">-NoWait</span></span>
<span data-ttu-id="893eb-152">Der Vorgang wird gestartet und unmittelbar vor Abschluss des Vorgangs beendet.</span><span class="sxs-lookup"><span data-stu-id="893eb-152">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="893eb-153">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="893eb-153">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893eb-154">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="893eb-154">-OrganizationName</span></span>
<span data-ttu-id="893eb-155">Gibt den Organisationsnamen der Erweiterung "Chef" an.</span><span class="sxs-lookup"><span data-stu-id="893eb-155">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="893eb-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="893eb-156">-ResourceGroupName</span></span>
<span data-ttu-id="893eb-157">Gibt den Namen der Ressourcengruppe an, die den virtuellen Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="893eb-157">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="893eb-158">-RunList</span><span class="sxs-lookup"><span data-stu-id="893eb-158">-RunList</span></span>
<span data-ttu-id="893eb-159">Gibt die Ausführungsliste des Knotens "Chef" an.</span><span class="sxs-lookup"><span data-stu-id="893eb-159">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="893eb-160">-Secret</span><span class="sxs-lookup"><span data-stu-id="893eb-160">-Secret</span></span>
<span data-ttu-id="893eb-161">Der Verschlüsselungsschlüssel, der zum Verschlüsseln und Entschlüsseln der Datentütenelementwerte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="893eb-161">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="893eb-162">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="893eb-162">-SecretFile</span></span>
<span data-ttu-id="893eb-163">Der Pfad zu der Datei, die den Verschlüsselungsschlüssel enthält, der zum Verschlüsseln und Entschlüsseln der Datentaschenelementwerte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="893eb-163">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="893eb-164">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="893eb-164">-TypeHandlerVersion</span></span>
<span data-ttu-id="893eb-165">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="893eb-165">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="893eb-166">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="893eb-166">-ValidationClientName</span></span>
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

### <span data-ttu-id="893eb-167">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="893eb-167">-ValidationPem</span></span>
<span data-ttu-id="893eb-168">Gibt den Dateipfad der Chef-Validator-PEM-Datei an.</span><span class="sxs-lookup"><span data-stu-id="893eb-168">Specifies the Chef validator .pem file path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="893eb-169">-VMName</span><span class="sxs-lookup"><span data-stu-id="893eb-169">-VMName</span></span>
<span data-ttu-id="893eb-170">Gibt den Namen eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="893eb-170">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="893eb-171">Dieses Cmdlet fügt die Erweiterung "Chef" für den virtuellen Computer hinzu, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="893eb-171">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="893eb-172">-Windows</span><span class="sxs-lookup"><span data-stu-id="893eb-172">-Windows</span></span>
<span data-ttu-id="893eb-173">Gibt an, dass mit diesem Cmdlet ein virtueller Windows-Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="893eb-173">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893eb-174">-Confirm</span><span class="sxs-lookup"><span data-stu-id="893eb-174">-Confirm</span></span>
<span data-ttu-id="893eb-175">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="893eb-175">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893eb-176">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="893eb-176">-WhatIf</span></span>
<span data-ttu-id="893eb-177">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="893eb-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="893eb-178">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="893eb-178">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893eb-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="893eb-179">CommonParameters</span></span>
<span data-ttu-id="893eb-180">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="893eb-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="893eb-181">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="893eb-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="893eb-182">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="893eb-182">INPUTS</span></span>

### <span data-ttu-id="893eb-183">System.String</span><span class="sxs-lookup"><span data-stu-id="893eb-183">System.String</span></span>

### <span data-ttu-id="893eb-184">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="893eb-184">System.Boolean</span></span>

## <span data-ttu-id="893eb-185">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="893eb-185">OUTPUTS</span></span>

### <span data-ttu-id="893eb-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="893eb-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="893eb-187">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="893eb-187">NOTES</span></span>

## <span data-ttu-id="893eb-188">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="893eb-188">RELATED LINKS</span></span>

[<span data-ttu-id="893eb-189">Get-AzVM ImmerExtension</span><span class="sxs-lookup"><span data-stu-id="893eb-189">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="893eb-190">Remove-AzVMAutomatExtension</span><span class="sxs-lookup"><span data-stu-id="893eb-190">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)
