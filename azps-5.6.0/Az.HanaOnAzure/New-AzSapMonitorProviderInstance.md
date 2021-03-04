---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/new-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
ms.openlocfilehash: eb84936310be355ece858884a1e27b7cc954cb51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949291"
---
# <span data-ttu-id="b54cc-101">New-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="b54cc-101">New-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="b54cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b54cc-102">SYNOPSIS</span></span>
<span data-ttu-id="b54cc-103">Erstellt eine Anbieterinstanz für das angegebene Abonnement, die Ressourcengruppe, den SapMonitor-Namen und den Ressourcennamen.</span><span class="sxs-lookup"><span data-stu-id="b54cc-103">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="b54cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b54cc-104">SYNTAX</span></span>

### <span data-ttu-id="b54cc-105">ByString (Standard)</span><span class="sxs-lookup"><span data-stu-id="b54cc-105">ByString (Default)</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b54cc-106">ByDict</span><span class="sxs-lookup"><span data-stu-id="b54cc-106">ByDict</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -InstanceProperty <Hashtable> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b54cc-107">ByKeyVault</span><span class="sxs-lookup"><span data-stu-id="b54cc-107">ByKeyVault</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b54cc-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b54cc-108">DESCRIPTION</span></span>
<span data-ttu-id="b54cc-109">Erstellt eine Anbieterinstanz für das angegebene Abonnement, die Ressourcengruppe, den SapMonitor-Namen und den Ressourcennamen.</span><span class="sxs-lookup"><span data-stu-id="b54cc-109">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="b54cc-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b54cc-110">EXAMPLES</span></span>

### <span data-ttu-id="b54cc-111">Beispiel 1: Erstellen einer Instanz eines SAP-Monitors nach Zeichenfolge für HANA</span><span class="sxs-lookup"><span data-stu-id="b54cc-111">Example 1: Create an instance of SAP monitor by string for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="b54cc-112">Mit diesem Befehl wird eine Instanz des SAP-Monitors nach Zeichenfolge für HANA erstellt.</span><span class="sxs-lookup"><span data-stu-id="b54cc-112">This command creates an instance of SAP monitor by string for HANA.</span></span>

### <span data-ttu-id="b54cc-113">Beispiel 2: Erstellen einer Instanz des SAP-Monitors nach Schlüsseltresor für HANA</span><span class="sxs-lookup"><span data-stu-id="b54cc-113">Example 2: Create an instance of SAP monitor by key vault for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="b54cc-114">Mit diesem Befehl wird eine Instanz des SAP-Monitors nach Schlüsseltresor für HANA erstellt.</span><span class="sxs-lookup"><span data-stu-id="b54cc-114">This command creates an instance of SAP monitor by key vault for HANA.</span></span>

### <span data-ttu-id="b54cc-115">Beispiel 3: Erstellen einer Instanz des SAP-Monitors nach Wörterbuch für PrometheusHaCluster</span><span class="sxs-lookup"><span data-stu-id="b54cc-115">Example 3: Create an instance of SAP monitor by dictionary for PrometheusHaCluster</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-promclt   -SapMonitorName dolauli-test04 -ProviderType PrometheusHaCluster -InstanceProperty @{prometheusUrl='http://10.4.1.10:9664/metrics'}


Name                     Type
----                     ----
dolauli-instance-promclt Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="b54cc-116">Mit diesem Befehl wird eine Instanz des SAP-Monitors nach Wörterbuch für PrometheusHaCluster erstellt.</span><span class="sxs-lookup"><span data-stu-id="b54cc-116">This command creates an instance of SAP monitor by dictionary for PrometheusHaCluster.</span></span>

### <span data-ttu-id="b54cc-117">Beispiel 4: Erstellen einer Instanz des SAP-Monitors nach Wörterbuch für PrometheusOS</span><span class="sxs-lookup"><span data-stu-id="b54cc-117">Example 4: Create an instance of SAP monitor by dictionary for PrometheusOS</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-prom   -SapMonitorName dolauli-test04 -ProviderType PrometheusOS -InstanceProperty @{prometheusUrl='http://10.3.1.6:9100/metrics'}

Name                  Type
----                  ----
dolauli-instance-prom Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="b54cc-118">Mit diesem Befehl wird eine Instanz des SAP-Monitors nach Wörterbuch für PrometheusOS erstellt.</span><span class="sxs-lookup"><span data-stu-id="b54cc-118">This command creates an instance of SAP monitor by dictionary for PrometheusOS.</span></span>

### <span data-ttu-id="b54cc-119">Beispiel 5: Erstellen einer Instanz des SAP-Monitors nach Wörterbuch für MsSqlServer</span><span class="sxs-lookup"><span data-stu-id="b54cc-119">Example 5: Create an instance of SAP monitor by dictionary for MsSqlServer</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-ms   -SapMonitorName dolauli-test04 -ProviderType MsSqlServer -InstanceProperty @{sqlHostname="10.4.8.90";sqlPort=1433;sqlUsername="AMFSS";sqlPassword="fakepassword"}

Name                Type
----                ----
dolauli-instance-ms Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="b54cc-120">Mit diesem Befehl wird eine Instanz des SAP-Monitors nach Wörterbuch für MsSqlServer erstellt.</span><span class="sxs-lookup"><span data-stu-id="b54cc-120">This command creates an instance of SAP monitor by dictionary for MsSqlServer.</span></span>

### <span data-ttu-id="b54cc-121">Beispiel 6: Erstellen einer Instanz des SAP-Monitors nach Wörterbuch für SapHana</span><span class="sxs-lookup"><span data-stu-id="b54cc-121">Example 6: Create an instance of SAP monitor by dictionary for SapHana</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-hana   -SapMonitorName dolauli-test04 -ProviderType SapHana -InstanceProperty @{hanaHostname="10.1.2.6";hanaDbName="SYSTEMDB";hanaDbSqlPort=30113;hanaDbUsername="SYSTEM"; hanaDbPassword="Manager1"}

Name                  Type
----                  ----
dolauli-instance-hana Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="b54cc-122">Mit diesem Befehl wird eine Instanz des SAP-Monitors nach Wörterbuch für SapHana erstellt.</span><span class="sxs-lookup"><span data-stu-id="b54cc-122">This command creates an instance of SAP monitor by dictionary for SapHana.</span></span>

## <span data-ttu-id="b54cc-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b54cc-123">PARAMETERS</span></span>

### <span data-ttu-id="b54cc-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b54cc-124">-AsJob</span></span>
<span data-ttu-id="b54cc-125">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="b54cc-125">Run the command as a job</span></span>

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

### <span data-ttu-id="b54cc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b54cc-126">-DefaultProfile</span></span>
<span data-ttu-id="b54cc-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b54cc-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b54cc-128">-HanaDatabaseName</span><span class="sxs-lookup"><span data-stu-id="b54cc-128">-HanaDatabaseName</span></span>
<span data-ttu-id="b54cc-129">Der Datenbankname der SAP HANA-Instanz.</span><span class="sxs-lookup"><span data-stu-id="b54cc-129">The database name of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b54cc-130">-HanaDatabasePassword</span><span class="sxs-lookup"><span data-stu-id="b54cc-130">-HanaDatabasePassword</span></span>
<span data-ttu-id="b54cc-131">Das Kennwort der Datenbank der SAP HANA-Instanz.</span><span class="sxs-lookup"><span data-stu-id="b54cc-131">The password of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByString
Aliases: HanaDbPassword

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b54cc-132">-HanaDatabasePasswordKeyVaultResourceId</span><span class="sxs-lookup"><span data-stu-id="b54cc-132">-HanaDatabasePasswordKeyVaultResourceId</span></span>
<span data-ttu-id="b54cc-133">Ressourcen-ID des Schlüsseltresor, der die HANA-Anmeldeinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="b54cc-133">Resource ID of the Key Vault that contains the HANA credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault
Aliases: HanaDbPasswordKeyVaultId, KeyVaultId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b54cc-134">-HanaDatabasePasswordSecretId</span><span class="sxs-lookup"><span data-stu-id="b54cc-134">-HanaDatabasePasswordSecretId</span></span>
<span data-ttu-id="b54cc-135">Geheimer Bezeichner des Schlüsseltresorschlüssels, der die HANA-Anmeldeinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="b54cc-135">Secret identifier to the Key Vault secret that contains the HANA credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault
Aliases: HanaDbPasswordSecretId, SecretId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b54cc-136">-HanaDatabaseSqlPort</span><span class="sxs-lookup"><span data-stu-id="b54cc-136">-HanaDatabaseSqlPort</span></span>
<span data-ttu-id="b54cc-137">Der SQL der Datenbank der SAP HANA-Instanz.</span><span class="sxs-lookup"><span data-stu-id="b54cc-137">The SQL port of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbSqlPort

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b54cc-138">-HanaDatabaseUsername</span><span class="sxs-lookup"><span data-stu-id="b54cc-138">-HanaDatabaseUsername</span></span>
<span data-ttu-id="b54cc-139">Der Benutzername der Datenbank der SAP HANA-Instanz.</span><span class="sxs-lookup"><span data-stu-id="b54cc-139">The username of the database of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbUsername

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b54cc-140">-HanaHostname</span><span class="sxs-lookup"><span data-stu-id="b54cc-140">-HanaHostname</span></span>
<span data-ttu-id="b54cc-141">Der Hostname der SAP HANA-Instanz.</span><span class="sxs-lookup"><span data-stu-id="b54cc-141">The hostname of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b54cc-142">-InstanceProperty</span><span class="sxs-lookup"><span data-stu-id="b54cc-142">-InstanceProperty</span></span>
<span data-ttu-id="b54cc-143">Die -Eigenschaft der HANA-Instanz.</span><span class="sxs-lookup"><span data-stu-id="b54cc-143">The property of HANA instance.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByDict
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b54cc-144">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="b54cc-144">-Metadata</span></span>
<span data-ttu-id="b54cc-145">Eine JSON-Zeichenfolge, die Metadaten der Anbieterinstanz enthält.</span><span class="sxs-lookup"><span data-stu-id="b54cc-145">A JSON string containing metadata of the provider instance.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b54cc-146">-Name</span><span class="sxs-lookup"><span data-stu-id="b54cc-146">-Name</span></span>
<span data-ttu-id="b54cc-147">Name der Anbieterinstanz.</span><span class="sxs-lookup"><span data-stu-id="b54cc-147">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b54cc-148">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b54cc-148">-NoWait</span></span>
<span data-ttu-id="b54cc-149">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="b54cc-149">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b54cc-150">-ProviderType</span><span class="sxs-lookup"><span data-stu-id="b54cc-150">-ProviderType</span></span>
<span data-ttu-id="b54cc-151">Der Typ der Anbieterinstanz.</span><span class="sxs-lookup"><span data-stu-id="b54cc-151">The type of provider instance.</span></span>
<span data-ttu-id="b54cc-152">Unterstützte Werte sind: "SapHana".</span><span class="sxs-lookup"><span data-stu-id="b54cc-152">Supported values are: "SapHana".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b54cc-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b54cc-153">-ResourceGroupName</span></span>
<span data-ttu-id="b54cc-154">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b54cc-154">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b54cc-155">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="b54cc-155">-SapMonitorName</span></span>
<span data-ttu-id="b54cc-156">Name der SAP-Monitorressource.</span><span class="sxs-lookup"><span data-stu-id="b54cc-156">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b54cc-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b54cc-157">-SubscriptionId</span></span>
<span data-ttu-id="b54cc-158">Abonnement-ID, mit der Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="b54cc-158">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b54cc-159">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="b54cc-159">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b54cc-160">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b54cc-160">-Confirm</span></span>
<span data-ttu-id="b54cc-161">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b54cc-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b54cc-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b54cc-162">-WhatIf</span></span>
<span data-ttu-id="b54cc-163">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b54cc-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b54cc-164">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b54cc-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b54cc-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b54cc-165">CommonParameters</span></span>
<span data-ttu-id="b54cc-166">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b54cc-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b54cc-167">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b54cc-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b54cc-168">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b54cc-168">INPUTS</span></span>

## <span data-ttu-id="b54cc-169">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b54cc-169">OUTPUTS</span></span>

### <span data-ttu-id="b54cc-170">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="b54cc-170">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="b54cc-171">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b54cc-171">NOTES</span></span>

<span data-ttu-id="b54cc-172">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b54cc-172">ALIASES</span></span>

## <span data-ttu-id="b54cc-173">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b54cc-173">RELATED LINKS</span></span>

