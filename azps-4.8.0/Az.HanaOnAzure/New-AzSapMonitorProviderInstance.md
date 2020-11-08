---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
ms.openlocfilehash: f0d8486bc26043ee4f2cb2126c7ffdc64829a7cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009261"
---
# <span data-ttu-id="14064-101">New-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="14064-101">New-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="14064-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="14064-102">SYNOPSIS</span></span>
<span data-ttu-id="14064-103">Erstellt eine Anbieterinstanz für das angegebene Abonnement, die Ressourcengruppe, den SapMonitor-Namen und den Ressourcennamen.</span><span class="sxs-lookup"><span data-stu-id="14064-103">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="14064-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="14064-104">SYNTAX</span></span>

### <span data-ttu-id="14064-105">ByString (Standard)</span><span class="sxs-lookup"><span data-stu-id="14064-105">ByString (Default)</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="14064-106">ByKeyVault</span><span class="sxs-lookup"><span data-stu-id="14064-106">ByKeyVault</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="14064-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14064-107">DESCRIPTION</span></span>
<span data-ttu-id="14064-108">Erstellt eine Anbieterinstanz für das angegebene Abonnement, die Ressourcengruppe, den SapMonitor-Namen und den Ressourcennamen.</span><span class="sxs-lookup"><span data-stu-id="14064-108">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="14064-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="14064-109">EXAMPLES</span></span>

### <span data-ttu-id="14064-110">Beispiel 1: Erstellen einer Instanz des SAP-Monitors anhand einer Zeichenfolge für Hana</span><span class="sxs-lookup"><span data-stu-id="14064-110">Example 1: Create an instance of SAP monitor by string for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="14064-111">Dieser Befehl erstellt eine Instanz des SAP-Monitors durch eine Zeichenfolge für Hana.</span><span class="sxs-lookup"><span data-stu-id="14064-111">This command creates an instance of SAP monitor by string for HANA.</span></span>

### <span data-ttu-id="14064-112">Beispiel 2: Erstellen einer Instanz des SAP-Monitors anhand des Schlüsseldepots für Hana</span><span class="sxs-lookup"><span data-stu-id="14064-112">Example 2: Create an instance of SAP monitor by key vault for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="14064-113">Mit diesem Befehl wird eine Instanz des SAP-Monitors von Key Vault für Hana erstellt.</span><span class="sxs-lookup"><span data-stu-id="14064-113">This command creates an instance of SAP monitor by key vault for HANA.</span></span>

## <span data-ttu-id="14064-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="14064-114">PARAMETERS</span></span>

### <span data-ttu-id="14064-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14064-115">-AsJob</span></span>
<span data-ttu-id="14064-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="14064-116">Run the command as a job</span></span>

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

### <span data-ttu-id="14064-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14064-117">-DefaultProfile</span></span>
<span data-ttu-id="14064-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="14064-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14064-119">-HanaDatabaseName</span><span class="sxs-lookup"><span data-stu-id="14064-119">-HanaDatabaseName</span></span>
<span data-ttu-id="14064-120">Der Datenbankname der SAP Hana-Instanz.</span><span class="sxs-lookup"><span data-stu-id="14064-120">The database name of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HanaDbName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14064-121">-HanaDatabasePassword</span><span class="sxs-lookup"><span data-stu-id="14064-121">-HanaDatabasePassword</span></span>
<span data-ttu-id="14064-122">Das Kennwort der Datenbank der SAP Hana-Instanz.</span><span class="sxs-lookup"><span data-stu-id="14064-122">The password of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="14064-123">-HanaDatabasePasswordKeyVaultResourceId</span><span class="sxs-lookup"><span data-stu-id="14064-123">-HanaDatabasePasswordKeyVaultResourceId</span></span>
<span data-ttu-id="14064-124">Die Ressourcen-ID des Schlüsseldepots, das die Hana-Anmeldeinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="14064-124">Resource ID of the Key Vault that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="14064-125">-HanaDatabasePasswordSecretId</span><span class="sxs-lookup"><span data-stu-id="14064-125">-HanaDatabasePasswordSecretId</span></span>
<span data-ttu-id="14064-126">Geheime Kennung für das Schlüsseldepot Secret, das die Hana-Anmeldeinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="14064-126">Secret identifier to the Key Vault secret that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="14064-127">-HanaDatabaseSqlPort</span><span class="sxs-lookup"><span data-stu-id="14064-127">-HanaDatabaseSqlPort</span></span>
<span data-ttu-id="14064-128">Der SQL-Port der Datenbank der SAP Hana-Instanz.</span><span class="sxs-lookup"><span data-stu-id="14064-128">The SQL port of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: HanaDbSqlPort

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14064-129">-HanaDatabaseUsername</span><span class="sxs-lookup"><span data-stu-id="14064-129">-HanaDatabaseUsername</span></span>
<span data-ttu-id="14064-130">Der Benutzername der Datenbank der SAP Hana-Instanz.</span><span class="sxs-lookup"><span data-stu-id="14064-130">The username of the database of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HanaDbUsername

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14064-131">-HanaHostname</span><span class="sxs-lookup"><span data-stu-id="14064-131">-HanaHostname</span></span>
<span data-ttu-id="14064-132">Der Hostname der SAP Hana-Instanz.</span><span class="sxs-lookup"><span data-stu-id="14064-132">The hostname of SAP HANA instance.</span></span>

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

### <span data-ttu-id="14064-133">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="14064-133">-Metadata</span></span>
<span data-ttu-id="14064-134">Eine JSON-Zeichenfolge mit Metadaten der Anbieterinstanz.</span><span class="sxs-lookup"><span data-stu-id="14064-134">A JSON string containing metadata of the provider instance.</span></span>

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

### <span data-ttu-id="14064-135">-Name</span><span class="sxs-lookup"><span data-stu-id="14064-135">-Name</span></span>
<span data-ttu-id="14064-136">Der Name der Anbieterinstanz.</span><span class="sxs-lookup"><span data-stu-id="14064-136">Name of the provider instance.</span></span>

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

### <span data-ttu-id="14064-137">-Nowait</span><span class="sxs-lookup"><span data-stu-id="14064-137">-NoWait</span></span>
<span data-ttu-id="14064-138">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="14064-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="14064-139">-ProviderType</span><span class="sxs-lookup"><span data-stu-id="14064-139">-ProviderType</span></span>
<span data-ttu-id="14064-140">Der Typ der Anbieterinstanz.</span><span class="sxs-lookup"><span data-stu-id="14064-140">The type of provider instance.</span></span>
<span data-ttu-id="14064-141">Unterstützte Werte sind: "SapHana".</span><span class="sxs-lookup"><span data-stu-id="14064-141">Supported values are: "SapHana".</span></span>

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

### <span data-ttu-id="14064-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14064-142">-ResourceGroupName</span></span>
<span data-ttu-id="14064-143">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="14064-143">Name of the resource group.</span></span>

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

### <span data-ttu-id="14064-144">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="14064-144">-SapMonitorName</span></span>
<span data-ttu-id="14064-145">Der Name der SAP-Monitor Ressource.</span><span class="sxs-lookup"><span data-stu-id="14064-145">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="14064-146">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="14064-146">-SubscriptionId</span></span>
<span data-ttu-id="14064-147">Abonnement-ID, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="14064-147">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="14064-148">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="14064-148">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="14064-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="14064-149">-Confirm</span></span>
<span data-ttu-id="14064-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="14064-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14064-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14064-151">-WhatIf</span></span>
<span data-ttu-id="14064-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="14064-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14064-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="14064-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14064-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14064-154">CommonParameters</span></span>
<span data-ttu-id="14064-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14064-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14064-156">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14064-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14064-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="14064-157">INPUTS</span></span>

## <span data-ttu-id="14064-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="14064-158">OUTPUTS</span></span>

### <span data-ttu-id="14064-159">Microsoft. Azure. PowerShell. Cmdlets. HanaOnAzure. Models. Api20200207Preview. IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="14064-159">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="14064-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="14064-160">NOTES</span></span>

<span data-ttu-id="14064-161">Aliase</span><span class="sxs-lookup"><span data-stu-id="14064-161">ALIASES</span></span>

## <span data-ttu-id="14064-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="14064-162">RELATED LINKS</span></span>

