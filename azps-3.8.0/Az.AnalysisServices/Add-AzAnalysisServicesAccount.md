---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/add-azanalysisservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
ms.openlocfilehash: f1d59a0a34072a91242c6595c269ba55c4397e0e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995889"
---
# <span data-ttu-id="69601-101">Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="69601-101">Add-AzAnalysisServicesAccount</span></span>

## <span data-ttu-id="69601-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="69601-102">SYNOPSIS</span></span>
<span data-ttu-id="69601-103">Fügt ein authentifiziertes Konto hinzu, das für Azure Analysis Services Server-Cmdlet-Anforderungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="69601-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

## <span data-ttu-id="69601-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="69601-104">SYNTAX</span></span>

### <span data-ttu-id="69601-105">UserParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="69601-105">UserParameterSetName (Default)</span></span>
```
Add-AzAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69601-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="69601-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69601-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="69601-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69601-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69601-108">DESCRIPTION</span></span>
<span data-ttu-id="69601-109">Das Add-AzAnalysisServicesAccount-Cmdlet wird für die Anmeldung bei einer Instanz von Azure Analysis Services-Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="69601-109">The Add-AzAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="69601-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="69601-110">EXAMPLES</span></span>

### <span data-ttu-id="69601-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="69601-111">Example 1</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="69601-112">In diesem Beispiel wird das von der $UserCredential-Variable angegebene Konto der westcentralus.asazure.Windows.net Analysis Services-Umgebung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="69601-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="69601-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="69601-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="69601-114">Der erste Befehl ruft die Anmeldeinformationen des Anwendungsdienst Prinzipals ab und speichert Sie dann in der $ApplicationCredential-Variablen.</span><span class="sxs-lookup"><span data-stu-id="69601-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="69601-115">Mit dem zweiten Befehl fügen Sie das von der $ApplicationCredential-Variable und der Mandanten-westcentralus.asazure.Windows.net angegebene Anwendungsdienst Prinzipal Konto zur Analysis Services-Umgebung hinzu.</span><span class="sxs-lookup"><span data-stu-id="69601-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="69601-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="69601-116">Example 3</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="69601-117">In diesem Beispiel wird das von der ApplicationId-, Tenant-und CertificateThumbprint-Anwendung angegebene Dienstprinzipal Konto der westcentralus.asazure.Windows.net Analysis Services-Umgebung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="69601-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="69601-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="69601-118">PARAMETERS</span></span>

### <span data-ttu-id="69601-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="69601-119">-ApplicationId</span></span>
<span data-ttu-id="69601-120">Die Anwendungs-ID.</span><span class="sxs-lookup"><span data-stu-id="69601-120">The application ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69601-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="69601-121">-CertificateThumbprint</span></span>
<span data-ttu-id="69601-122">Zertifikat Hash (Fingerabdruck)</span><span class="sxs-lookup"><span data-stu-id="69601-122">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69601-123">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="69601-123">-Credential</span></span>
<span data-ttu-id="69601-124">Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="69601-124">Login credentials</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithPasswordParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69601-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="69601-125">-RolloutEnvironment</span></span>
<span data-ttu-id="69601-126">Der Name der Azure Analysis Services-Umgebung, an der Sie sich anmelden möchten.</span><span class="sxs-lookup"><span data-stu-id="69601-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="69601-127">Bei Angabe des vollständigen Namens des Servers, beispielsweise asazure://westcentralus.asazure.Windows.net/Testserver, wird der richtige Wert für diese Variable westcentralus.asazure.Windows.net.</span><span class="sxs-lookup"><span data-stu-id="69601-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

```yaml
Type: System.String
Parameter Sets: UserParameterSetName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69601-128">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="69601-128">-ServicePrincipal</span></span>
<span data-ttu-id="69601-129">Gibt an, dass sich dieses Konto durch die Bereitstellung von Dienstprinzipal Anmeldeinformationen authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="69601-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69601-130">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="69601-130">-TenantId</span></span>
<span data-ttu-id="69601-131">Mandantenname oder-ID</span><span class="sxs-lookup"><span data-stu-id="69601-131">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69601-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="69601-132">-Confirm</span></span>
<span data-ttu-id="69601-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="69601-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69601-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69601-134">-WhatIf</span></span>
<span data-ttu-id="69601-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69601-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69601-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="69601-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69601-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69601-137">CommonParameters</span></span>
<span data-ttu-id="69601-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69601-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69601-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69601-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69601-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="69601-140">INPUTS</span></span>

### <span data-ttu-id="69601-141">Keine</span><span class="sxs-lookup"><span data-stu-id="69601-141">None</span></span>

## <span data-ttu-id="69601-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="69601-142">OUTPUTS</span></span>

### <span data-ttu-id="69601-143">Microsoft. Azure. Commands. AnalysisServices. dataplane. AsAzureProfile</span><span class="sxs-lookup"><span data-stu-id="69601-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="69601-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="69601-144">NOTES</span></span>
<span data-ttu-id="69601-145">Alias: Login-AzAsAccount</span><span class="sxs-lookup"><span data-stu-id="69601-145">Alias: Login-AzAsAccount</span></span>

## <span data-ttu-id="69601-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="69601-146">RELATED LINKS</span></span>
