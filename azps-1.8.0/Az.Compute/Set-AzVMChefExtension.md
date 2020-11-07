---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
ms.openlocfilehash: b26ce11a60894ae8bf43b49c1395b4683b0280fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661441"
---
# <span data-ttu-id="2fa3e-101">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="2fa3e-101">Set-AzVMChefExtension</span></span>

## <span data-ttu-id="2fa3e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2fa3e-102">SYNOPSIS</span></span>
<span data-ttu-id="2fa3e-103">Fügt eine Erweiterung des Chefkochs zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-103">Adds a Chef extension to a virtual machine.</span></span>

## <span data-ttu-id="2fa3e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fa3e-104">SYNTAX</span></span>

### <span data-ttu-id="2fa3e-105">Linux</span><span class="sxs-lookup"><span data-stu-id="2fa3e-105">Linux</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2fa3e-106">Windows</span><span class="sxs-lookup"><span data-stu-id="2fa3e-106">Windows</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2fa3e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2fa3e-107">DESCRIPTION</span></span>
<span data-ttu-id="2fa3e-108">Das Cmdlet " **Satz-AzVMChefExtension** " fügt der virtuellen Maschine die Erweiterung "Chef" hinzu.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-108">The **Set-AzVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="2fa3e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2fa3e-109">EXAMPLES</span></span>

### <span data-ttu-id="2fa3e-110">Beispiel 1: Hinzufügen einer Chefkoch-Erweiterung zu einem virtuellen Windows-Computer</span><span class="sxs-lookup"><span data-stu-id="2fa3e-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="2fa3e-111">Mit diesem Befehl wird eine Erweiterung des Chefkochs zu einem virtuellen Windows-Computer mit dem Namen WindowsVM001 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="2fa3e-112">Wenn der virtuelle Computer gestartet wird, startet der Chefkoch den virtuellen Computer, um Apache auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="2fa3e-113">Beispiel 2: Hinzufügen einer Chefkoch-Erweiterung zu einem virtuellen Linux-Computer</span><span class="sxs-lookup"><span data-stu-id="2fa3e-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="2fa3e-114">Mit diesem Befehl wird eine Erweiterung des Chefkochs zu einem virtuellen Linux-Computer mit dem Namen LinuxVM001 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="2fa3e-115">Wenn der virtuelle Computer gestartet wird, startet der Chefkoch den virtuellen Computer, um Apache auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="2fa3e-116">Beispiel 3: Hinzufügen einer Chefkoch-Erweiterung zu einem virtuellen Windows-Computer mit Bootstrap-Optionen</span><span class="sxs-lookup"><span data-stu-id="2fa3e-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="2fa3e-117">Mit diesem Befehl wird die Erweiterung des Chefkochs zu einem virtuellen Windows-Computer mit dem Namen WindowsVM002 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="2fa3e-118">Wenn der virtuelle Computer gestartet wird, startet der Chefkoch den virtuellen Computer, um Apache auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="2fa3e-119">Nach dem Bootstrapping verweist der virtuelle Computer auf die im JSON-Format angegebenen bootstrapoptions.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="2fa3e-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fa3e-120">PARAMETERS</span></span>

### <span data-ttu-id="2fa3e-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2fa3e-121">-AutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="2fa3e-122">-Bootstrapoptions</span><span class="sxs-lookup"><span data-stu-id="2fa3e-122">-BootstrapOptions</span></span>
<span data-ttu-id="2fa3e-123">Gibt die Konfigurationseinstellungen in der Option client_rb an.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-123">Specifies configuration settings in the client_rb option.</span></span>

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

### <span data-ttu-id="2fa3e-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="2fa3e-124">-BootstrapVersion</span></span>
<span data-ttu-id="2fa3e-125">Gibt die Version der Bootstrap-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-125">Specifies the version of the bootstrap configuration.</span></span>

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

### <span data-ttu-id="2fa3e-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="2fa3e-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="2fa3e-127">Gibt die Häufigkeit (in Minuten) an, auf der der Chef-Service ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="2fa3e-128">Wenn Sie nicht möchten, dass der Chef-Service auf dem Azure VM installiert wird, setzen Sie in diesem Feld den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

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

### <span data-ttu-id="2fa3e-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="2fa3e-129">-ChefServerUrl</span></span>
<span data-ttu-id="2fa3e-130">Gibt den Chefkoch-Server Link als URL an.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-130">Specifies the Chef server link, as a URL.</span></span>

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

### <span data-ttu-id="2fa3e-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="2fa3e-131">-ClientRb</span></span>
<span data-ttu-id="2fa3e-132">Gibt den vollständigen Pfad des Chefkoch-Clients. RB an.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-132">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="2fa3e-133">-Daemon</span><span class="sxs-lookup"><span data-stu-id="2fa3e-133">-Daemon</span></span>
<span data-ttu-id="2fa3e-134">Konfiguriert den Chef-Client Dienst für die unbeaufsichtigte Ausführung.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="2fa3e-135">Die Knoten Plattform sollte Windows sein.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-135">The node platform should be Windows.</span></span>
<span data-ttu-id="2fa3e-136">Zulässige Optionen: "keine", "Dienst" und "Aufgabe".</span><span class="sxs-lookup"><span data-stu-id="2fa3e-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="2fa3e-137">keine – zurzeit wird verhindert, dass der Chef-Client-Dienst als Dienst konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="2fa3e-138">Dienst – konfiguriert den Chef-Client so, dass er automatisch im Hintergrund als Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="2fa3e-139">Aufgabe – konfiguriert den Chef-Client so, dass er automatisch im Hintergrund als secheduled-Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-139">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

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

### <span data-ttu-id="2fa3e-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fa3e-140">-DefaultProfile</span></span>
<span data-ttu-id="2fa3e-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fa3e-142">-Jsonattribute</span><span class="sxs-lookup"><span data-stu-id="2fa3e-142">-JsonAttribute</span></span>
<span data-ttu-id="2fa3e-143">Eine JSON-Zeichenfolge, die der ersten Ausführung von Chef-Client hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="2fa3e-144">beispielsweise-jsonattribute ' {"foo": "Leiste"} '</span><span class="sxs-lookup"><span data-stu-id="2fa3e-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="2fa3e-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="2fa3e-145">-Linux</span></span>
<span data-ttu-id="2fa3e-146">Gibt an, dass dieses Cmdlet einen virtuellen Windows-Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="2fa3e-147">-Standort</span><span class="sxs-lookup"><span data-stu-id="2fa3e-147">-Location</span></span>
<span data-ttu-id="2fa3e-148">Gibt den Speicherort der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-148">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="2fa3e-149">-Name</span><span class="sxs-lookup"><span data-stu-id="2fa3e-149">-Name</span></span>
<span data-ttu-id="2fa3e-150">Gibt den Namen der Erweiterung "Chef" an.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-150">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="2fa3e-151">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="2fa3e-151">-OrganizationName</span></span>
<span data-ttu-id="2fa3e-152">Gibt den Organisationsnamen der Erweiterung "Chef" an.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-152">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="2fa3e-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fa3e-153">-ResourceGroupName</span></span>
<span data-ttu-id="2fa3e-154">Gibt den Namen der Ressourcengruppe an, die den virtuellen Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-154">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="2fa3e-155">-RunList</span><span class="sxs-lookup"><span data-stu-id="2fa3e-155">-RunList</span></span>
<span data-ttu-id="2fa3e-156">Gibt die Liste "Leiter Knoten ausführen" an.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-156">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="2fa3e-157">-Secret</span><span class="sxs-lookup"><span data-stu-id="2fa3e-157">-Secret</span></span>
<span data-ttu-id="2fa3e-158">Der Verschlüsselungsschlüssel, der zum Verschlüsseln und Entschlüsseln der Daten Beutel-Elementwerte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-158">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="2fa3e-159">-Secretdatei</span><span class="sxs-lookup"><span data-stu-id="2fa3e-159">-SecretFile</span></span>
<span data-ttu-id="2fa3e-160">Der Pfad zu der Datei, die den Verschlüsselungsschlüssel enthält, der zum Verschlüsseln und Entschlüsseln der Daten Beutel-Elementwerte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-160">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="2fa3e-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2fa3e-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="2fa3e-162">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-162">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="2fa3e-163">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="2fa3e-163">-ValidationClientName</span></span>
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

### <span data-ttu-id="2fa3e-164">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="2fa3e-164">-ValidationPem</span></span>
<span data-ttu-id="2fa3e-165">Gibt den "Chef Validator. PEM"-Dateipfad an</span><span class="sxs-lookup"><span data-stu-id="2fa3e-165">Specifies the Chef validator .pem file path</span></span>

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

### <span data-ttu-id="2fa3e-166">-VMName</span><span class="sxs-lookup"><span data-stu-id="2fa3e-166">-VMName</span></span>
<span data-ttu-id="2fa3e-167">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-167">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="2fa3e-168">Mit diesem Cmdlet wird die Erweiterung "Chef" für den virtuellen Computer, den dieser Parameter angibt, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-168">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="2fa3e-169">-Windows</span><span class="sxs-lookup"><span data-stu-id="2fa3e-169">-Windows</span></span>
<span data-ttu-id="2fa3e-170">Gibt an, dass dieses Cmdlet einen virtuellen Windows-Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-170">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="2fa3e-171">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2fa3e-171">-Confirm</span></span>
<span data-ttu-id="2fa3e-172">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fa3e-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fa3e-173">-WhatIf</span></span>
<span data-ttu-id="2fa3e-174">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fa3e-175">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fa3e-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fa3e-176">CommonParameters</span></span>
<span data-ttu-id="2fa3e-177">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fa3e-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fa3e-178">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fa3e-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fa3e-179">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2fa3e-179">INPUTS</span></span>

### <span data-ttu-id="2fa3e-180">System. String</span><span class="sxs-lookup"><span data-stu-id="2fa3e-180">System.String</span></span>

### <span data-ttu-id="2fa3e-181">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2fa3e-181">System.Boolean</span></span>

## <span data-ttu-id="2fa3e-182">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2fa3e-182">OUTPUTS</span></span>

### <span data-ttu-id="2fa3e-183">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2fa3e-183">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2fa3e-184">Notizen</span><span class="sxs-lookup"><span data-stu-id="2fa3e-184">NOTES</span></span>

## <span data-ttu-id="2fa3e-185">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2fa3e-185">RELATED LINKS</span></span>

[<span data-ttu-id="2fa3e-186">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="2fa3e-186">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="2fa3e-187">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="2fa3e-187">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)
