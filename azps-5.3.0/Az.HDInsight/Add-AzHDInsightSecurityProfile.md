---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
ms.openlocfilehash: c44fea946f98c6ac19e77e7012910afac37bff7c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469700"
---
# <span data-ttu-id="48b19-101">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="48b19-101">Add-AzHDInsightSecurityProfile</span></span>

## <span data-ttu-id="48b19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48b19-102">SYNOPSIS</span></span>
<span data-ttu-id="48b19-103">Fügt einem Clusterkonfigurationsobjekt ein Sicherheitsprofil hinzu.</span><span class="sxs-lookup"><span data-stu-id="48b19-103">Adds a security profile to a cluster configuration object.</span></span>

## <span data-ttu-id="48b19-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48b19-104">SYNTAX</span></span>

```
Add-AzHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -DomainResourceId <String>
 -DomainUserCredential <PSCredential> [-OrganizationalUnitDN <String>] -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48b19-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48b19-105">DESCRIPTION</span></span>
<span data-ttu-id="48b19-106">Sicherheitsprofil wird zum Erstellen eines sicheren Clusters verwendet, indem es durch Unfällig wird.</span><span class="sxs-lookup"><span data-stu-id="48b19-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="48b19-107">Das Sicherheitsprofil enthält konfigurationsbezogene Verbindungen zwischen dem Cluster und der Active Directory-Domäne.</span><span class="sxs-lookup"><span data-stu-id="48b19-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="48b19-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="48b19-108">EXAMPLES</span></span>

### <span data-ttu-id="48b19-109">Beispiel 1: Hinzufügen eines Sicherheitsprofils zum Clusterkonfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="48b19-109">Example 1: Add security profile to the cluster configuration object</span></span>
```
PS C:\> #Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value

PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

#Security profile info
PS C:\> $domain="sampledomain.onmicrosoft.com"
PS C:\> $domainUser="sample.user@sampledomain.onmicrosoft.com"
PS C:\> $domainPassword=ConvertTo-SecureString "domainPassword" -AsPlainText -Force
PS C:\> $domainUserCredential=New-Object System.Management.Automation.PSCredential($domainUser, $domainPassword)
PS C:\> $organizationalUnitDN="ou=testunitdn"
PS C:\> $ldapsUrls=("ldaps://sampledomain.onmicrosoft.com:636","ldaps://sampledomain.onmicrosoft.com:389")
PS C:\> $clusterUsersGroupDNs=("groupdn1","groupdn2")

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightSecurityProfile `
                -Domain $domain `
                -DomainUserCredential $domainUserCredential `
                -OrganizationalUnitDN $organizationalUnitDN `
                -LdapsUrls $ldapsUrls `
                -ClusterUsersGroupDNs $clusterUsersGroupDNs `
            | New-AzHDInsightCluster `
                -ClusterType Spark `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="48b19-110">Dieser Befehl fügt dem Cluster einen Sicherheitsprofilwert namens "Ihr-Hadoop-001" hinzu.</span><span class="sxs-lookup"><span data-stu-id="48b19-110">This command adds a security profile value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="48b19-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48b19-111">PARAMETERS</span></span>

### <span data-ttu-id="48b19-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="48b19-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="48b19-113">Distinguished names of the Active Directory groups that will be available in Einemari and Ranger</span><span class="sxs-lookup"><span data-stu-id="48b19-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b19-114">-Config</span><span class="sxs-lookup"><span data-stu-id="48b19-114">-Config</span></span>
<span data-ttu-id="48b19-115">Gibt das Konfigurationsobjekt für den HDInsight-Cluster an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="48b19-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="48b19-116">Dieses Objekt wird vom New-AzHDInsightClusterConfig erstellt.</span><span class="sxs-lookup"><span data-stu-id="48b19-116">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48b19-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48b19-117">-DefaultProfile</span></span>
<span data-ttu-id="48b19-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="48b19-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48b19-119">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="48b19-119">-DomainResourceId</span></span>
<span data-ttu-id="48b19-120">Active Directory-Domänenressourcen-ID für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="48b19-120">Active Directory domain resource id for the cluster.</span></span>

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

### <span data-ttu-id="48b19-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="48b19-121">-DomainUserCredential</span></span>
<span data-ttu-id="48b19-122">Anmeldeinformationen eines Domänenbenutzerkontos mit ausreichenden Berechtigungen zum Erstellen des Cluster.</span><span class="sxs-lookup"><span data-stu-id="48b19-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="48b19-123">Benutzername sollte im Format user@domain vorliegen</span><span class="sxs-lookup"><span data-stu-id="48b19-123">Username should be in user@domain format</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b19-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="48b19-124">-LdapsUrls</span></span>
<span data-ttu-id="48b19-125">Urls eines oder mehrerer LDAPS-Server für Active Directory</span><span class="sxs-lookup"><span data-stu-id="48b19-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b19-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="48b19-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="48b19-127">Distinguished name of the organizational unit in the Active Directory where user and computer accounts will be created</span><span class="sxs-lookup"><span data-stu-id="48b19-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b19-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48b19-128">-Confirm</span></span>
<span data-ttu-id="48b19-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="48b19-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48b19-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="48b19-130">-WhatIf</span></span>
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

### <span data-ttu-id="48b19-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48b19-131">CommonParameters</span></span>
<span data-ttu-id="48b19-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48b19-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48b19-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48b19-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48b19-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="48b19-134">INPUTS</span></span>

### <span data-ttu-id="48b19-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="48b19-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
## <span data-ttu-id="48b19-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="48b19-136">OUTPUTS</span></span>

### <span data-ttu-id="48b19-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="48b19-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>
## <span data-ttu-id="48b19-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="48b19-138">NOTES</span></span>

## <span data-ttu-id="48b19-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="48b19-139">RELATED LINKS</span></span>
