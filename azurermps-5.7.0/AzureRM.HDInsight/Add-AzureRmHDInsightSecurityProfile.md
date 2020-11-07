---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
ms.openlocfilehash: 41571439400810214bee7f0f3f646e6444998982
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662735"
---
# <span data-ttu-id="ad440-101">Add-AzureRmHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="ad440-101">Add-AzureRmHDInsightSecurityProfile</span></span>

## <span data-ttu-id="ad440-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad440-102">SYNOPSIS</span></span>
<span data-ttu-id="ad440-103">Fügt ein Security profileo-Cluster-Konfigurationsobjekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="ad440-103">Adds a security profileto a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad440-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad440-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -Domain <String>
 -DomainUserCredential <PSCredential> -OrganizationalUnitDN <String> -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad440-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad440-105">DESCRIPTION</span></span>
<span data-ttu-id="ad440-106">Das Sicherheitsprofil wird verwendet, um ein sicheres Cluster zu erstellen, indem Sie es kerberizing.</span><span class="sxs-lookup"><span data-stu-id="ad440-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="ad440-107">Das Sicherheitsprofil enthält die Konfiguration, die dem Cluster Beitritt zur Active Directory-Domäne entspricht.</span><span class="sxs-lookup"><span data-stu-id="ad440-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="ad440-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad440-108">EXAMPLES</span></span>

### <span data-ttu-id="ad440-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ad440-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ad440-110">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="ad440-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="ad440-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad440-111">PARAMETERS</span></span>

### <span data-ttu-id="ad440-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="ad440-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="ad440-113">Definierte Namen der Active Directory-Gruppen, die in Ambari und Ranger verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="ad440-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad440-114">-Config</span><span class="sxs-lookup"><span data-stu-id="ad440-114">-Config</span></span>
<span data-ttu-id="ad440-115">Gibt das HDInsight-Cluster Konfigurationsobjekt an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="ad440-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="ad440-116">Dieses Objekt wird vom New-AzureRmHDInsightClusterConfig-Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="ad440-116">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad440-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad440-117">-DefaultProfile</span></span>
<span data-ttu-id="ad440-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ad440-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad440-119">-Domäne</span><span class="sxs-lookup"><span data-stu-id="ad440-119">-Domain</span></span>
<span data-ttu-id="ad440-120">Active Directory-Domäne für den Cluster</span><span class="sxs-lookup"><span data-stu-id="ad440-120">Active Directory domain for the cluster</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad440-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="ad440-121">-DomainUserCredential</span></span>
<span data-ttu-id="ad440-122">Ein Domänenbenutzerkonto, das über ausreichende Berechtigungen zum Erstellen des Clusters verfügt.</span><span class="sxs-lookup"><span data-stu-id="ad440-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="ad440-123">Der Benutzername sollte im user@domain Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="ad440-123">Username should be in user@domain format</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad440-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="ad440-124">-LdapsUrls</span></span>
<span data-ttu-id="ad440-125">URLs von einem oder mehreren LDAPS-Servern für Active Directory</span><span class="sxs-lookup"><span data-stu-id="ad440-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad440-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="ad440-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="ad440-127">Distinguished Name der Organisationseinheit in Active Directory, in der Benutzer-und Computerkonten erstellt werden</span><span class="sxs-lookup"><span data-stu-id="ad440-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad440-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ad440-128">-Confirm</span></span>
<span data-ttu-id="ad440-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ad440-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad440-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad440-130">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad440-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad440-131">CommonParameters</span></span>
<span data-ttu-id="ad440-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad440-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad440-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad440-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad440-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad440-134">INPUTS</span></span>

### <span data-ttu-id="ad440-135">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="ad440-135">AzureHDInsightConfig</span></span>
<span data-ttu-id="ad440-136">Der Parameter "config" akzeptiert den Wert vom Typ "AzureHDInsightConfig" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ad440-136">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="ad440-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad440-137">OUTPUTS</span></span>

### <span data-ttu-id="ad440-138">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="ad440-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>

## <span data-ttu-id="ad440-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad440-139">NOTES</span></span>

## <span data-ttu-id="ad440-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad440-140">RELATED LINKS</span></span>

