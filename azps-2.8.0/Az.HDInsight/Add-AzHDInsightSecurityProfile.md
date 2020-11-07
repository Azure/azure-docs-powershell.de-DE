---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
ms.openlocfilehash: c0e54e92336b7b084448a980f632c886c24dc07c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651085"
---
# <span data-ttu-id="aac03-101">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="aac03-101">Add-AzHDInsightSecurityProfile</span></span>

## <span data-ttu-id="aac03-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aac03-102">SYNOPSIS</span></span>
<span data-ttu-id="aac03-103">Fügt einem Cluster Konfigurationsobjekt ein Sicherheitsprofil hinzu.</span><span class="sxs-lookup"><span data-stu-id="aac03-103">Adds a security profile to a cluster configuration object.</span></span>

## <span data-ttu-id="aac03-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aac03-104">SYNTAX</span></span>

```
Add-AzHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -Domain <String>
 -DomainUserCredential <PSCredential> -OrganizationalUnitDN <String> -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aac03-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aac03-105">DESCRIPTION</span></span>
<span data-ttu-id="aac03-106">Das Sicherheitsprofil wird verwendet, um ein sicheres Cluster zu erstellen, indem Sie es kerberizing.</span><span class="sxs-lookup"><span data-stu-id="aac03-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="aac03-107">Das Sicherheitsprofil enthält die Konfiguration, die dem Cluster Beitritt zur Active Directory-Domäne entspricht.</span><span class="sxs-lookup"><span data-stu-id="aac03-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="aac03-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aac03-108">EXAMPLES</span></span>

### <span data-ttu-id="aac03-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aac03-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="aac03-110">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="aac03-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="aac03-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="aac03-111">PARAMETERS</span></span>

### <span data-ttu-id="aac03-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="aac03-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="aac03-113">Definierte Namen der Active Directory-Gruppen, die in Ambari und Ranger verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="aac03-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

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

### <span data-ttu-id="aac03-114">-Config</span><span class="sxs-lookup"><span data-stu-id="aac03-114">-Config</span></span>
<span data-ttu-id="aac03-115">Gibt das HDInsight-Cluster Konfigurationsobjekt an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="aac03-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="aac03-116">Dieses Objekt wird vom New-AzHDInsightClusterConfig-Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="aac03-116">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="aac03-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aac03-117">-DefaultProfile</span></span>
<span data-ttu-id="aac03-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="aac03-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aac03-119">-Domäne</span><span class="sxs-lookup"><span data-stu-id="aac03-119">-Domain</span></span>
<span data-ttu-id="aac03-120">Active Directory-Domäne für den Cluster</span><span class="sxs-lookup"><span data-stu-id="aac03-120">Active Directory domain for the cluster</span></span>

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

### <span data-ttu-id="aac03-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="aac03-121">-DomainUserCredential</span></span>
<span data-ttu-id="aac03-122">Ein Domänenbenutzerkonto, das über ausreichende Berechtigungen zum Erstellen des Clusters verfügt.</span><span class="sxs-lookup"><span data-stu-id="aac03-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="aac03-123">Der Benutzername sollte im user@domain Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="aac03-123">Username should be in user@domain format</span></span>

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

### <span data-ttu-id="aac03-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="aac03-124">-LdapsUrls</span></span>
<span data-ttu-id="aac03-125">URLs von einem oder mehreren LDAPS-Servern für Active Directory</span><span class="sxs-lookup"><span data-stu-id="aac03-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

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

### <span data-ttu-id="aac03-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="aac03-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="aac03-127">Distinguished Name der Organisationseinheit in Active Directory, in der Benutzer-und Computerkonten erstellt werden</span><span class="sxs-lookup"><span data-stu-id="aac03-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

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

### <span data-ttu-id="aac03-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aac03-128">-Confirm</span></span>
<span data-ttu-id="aac03-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aac03-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aac03-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aac03-130">-WhatIf</span></span>
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

### <span data-ttu-id="aac03-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac03-131">CommonParameters</span></span>
<span data-ttu-id="aac03-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aac03-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac03-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aac03-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac03-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aac03-134">INPUTS</span></span>

### <span data-ttu-id="aac03-135">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="aac03-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="aac03-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aac03-136">OUTPUTS</span></span>

### <span data-ttu-id="aac03-137">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="aac03-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>

## <span data-ttu-id="aac03-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="aac03-138">NOTES</span></span>

## <span data-ttu-id="aac03-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aac03-139">RELATED LINKS</span></span>
