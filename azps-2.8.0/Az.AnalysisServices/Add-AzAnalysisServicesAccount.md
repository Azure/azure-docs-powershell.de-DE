---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/add-azanalysisservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
ms.openlocfilehash: 323e7dd08c2ec18598f089a8001b6d06970b5600
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658377"
---
# <span data-ttu-id="431ee-101">Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="431ee-101">Add-AzAnalysisServicesAccount</span></span>

## <span data-ttu-id="431ee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="431ee-102">SYNOPSIS</span></span>
<span data-ttu-id="431ee-103">Fügt ein authentifiziertes Konto hinzu, das für Azure Analysis Services Server-Cmdlet-Anforderungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="431ee-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

## <span data-ttu-id="431ee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="431ee-104">SYNTAX</span></span>

### <span data-ttu-id="431ee-105">UserParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="431ee-105">UserParameterSetName (Default)</span></span>
```
Add-AzAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="431ee-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="431ee-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="431ee-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="431ee-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="431ee-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="431ee-108">DESCRIPTION</span></span>
<span data-ttu-id="431ee-109">Das Add-AzAnalysisServicesAccount-Cmdlet wird für die Anmeldung bei einer Instanz von Azure Analysis Services-Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="431ee-109">The Add-AzAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="431ee-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="431ee-110">EXAMPLES</span></span>

### <span data-ttu-id="431ee-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="431ee-111">Example 1</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="431ee-112">In diesem Beispiel wird das von der $UserCredential-Variable angegebene Konto der westcentralus.asazure.Windows.net Analysis Services-Umgebung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="431ee-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="431ee-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="431ee-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="431ee-114">Der erste Befehl ruft die Anmeldeinformationen des Anwendungsdienst Prinzipals ab und speichert Sie dann in der $ApplicationCredential-Variablen.</span><span class="sxs-lookup"><span data-stu-id="431ee-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="431ee-115">Mit dem zweiten Befehl fügen Sie das von der $ApplicationCredential-Variable und der Mandanten-westcentralus.asazure.Windows.net angegebene Anwendungsdienst Prinzipal Konto zur Analysis Services-Umgebung hinzu.</span><span class="sxs-lookup"><span data-stu-id="431ee-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="431ee-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="431ee-116">Example 3</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="431ee-117">In diesem Beispiel wird das von der ApplicationId-, Tenant-und CertificateThumbprint-Anwendung angegebene Dienstprinzipal Konto der westcentralus.asazure.Windows.net Analysis Services-Umgebung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="431ee-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="431ee-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="431ee-118">PARAMETERS</span></span>

### <span data-ttu-id="431ee-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="431ee-119">-ApplicationId</span></span>
<span data-ttu-id="431ee-120">Die Anwendungs-ID.</span><span class="sxs-lookup"><span data-stu-id="431ee-120">The application ID.</span></span>

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

### <span data-ttu-id="431ee-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="431ee-121">-CertificateThumbprint</span></span>
<span data-ttu-id="431ee-122">Zertifikat Hash (Fingerabdruck)</span><span class="sxs-lookup"><span data-stu-id="431ee-122">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="431ee-123">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="431ee-123">-Credential</span></span>
<span data-ttu-id="431ee-124">Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="431ee-124">Login credentials</span></span>

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

### <span data-ttu-id="431ee-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="431ee-125">-RolloutEnvironment</span></span>
<span data-ttu-id="431ee-126">Der Name der Azure Analysis Services-Umgebung, an der Sie sich anmelden möchten.</span><span class="sxs-lookup"><span data-stu-id="431ee-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="431ee-127">Bei Angabe des vollständigen Namens des Servers, beispielsweise asazure://westcentralus.asazure.Windows.net/Testserver, wird der richtige Wert für diese Variable westcentralus.asazure.Windows.net.</span><span class="sxs-lookup"><span data-stu-id="431ee-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

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

### <span data-ttu-id="431ee-128">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="431ee-128">-ServicePrincipal</span></span>
<span data-ttu-id="431ee-129">Gibt an, dass sich dieses Konto durch die Bereitstellung von Dienstprinzipal Anmeldeinformationen authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="431ee-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="431ee-130">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="431ee-130">-TenantId</span></span>
<span data-ttu-id="431ee-131">Mandantenname oder-ID</span><span class="sxs-lookup"><span data-stu-id="431ee-131">Tenant name or ID</span></span>

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

### <span data-ttu-id="431ee-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="431ee-132">-Confirm</span></span>
<span data-ttu-id="431ee-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="431ee-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="431ee-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="431ee-134">-WhatIf</span></span>
<span data-ttu-id="431ee-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="431ee-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="431ee-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="431ee-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="431ee-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="431ee-137">CommonParameters</span></span>
<span data-ttu-id="431ee-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="431ee-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="431ee-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="431ee-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="431ee-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="431ee-140">INPUTS</span></span>

### <span data-ttu-id="431ee-141">Keine</span><span class="sxs-lookup"><span data-stu-id="431ee-141">None</span></span>

## <span data-ttu-id="431ee-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="431ee-142">OUTPUTS</span></span>

### <span data-ttu-id="431ee-143">Microsoft. Azure. Commands. AnalysisServices. dataplane. AsAzureProfile</span><span class="sxs-lookup"><span data-stu-id="431ee-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="431ee-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="431ee-144">NOTES</span></span>
<span data-ttu-id="431ee-145">Alias: Login-AzAsAccount</span><span class="sxs-lookup"><span data-stu-id="431ee-145">Alias: Login-AzAsAccount</span></span>

## <span data-ttu-id="431ee-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="431ee-146">RELATED LINKS</span></span>
