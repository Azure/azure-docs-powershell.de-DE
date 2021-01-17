---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
ms.openlocfilehash: 46977fe6b2e6cf3c3811c7d9bbd49262b06cec54
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459343"
---
# <span data-ttu-id="96f5b-101">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="96f5b-101">New-AzADSpCredential</span></span>

## <span data-ttu-id="96f5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96f5b-102">SYNOPSIS</span></span>
<span data-ttu-id="96f5b-103">Fügt einem vorhandenen Dienstprinzipal Anmeldeinformationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="96f5b-103">Adds a credential to an existing service principal.</span></span>

## <span data-ttu-id="96f5b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96f5b-104">SYNTAX</span></span>

### <span data-ttu-id="96f5b-105">SpObjectIdWithPasswordParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="96f5b-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADSpCredential -ObjectId <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96f5b-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="96f5b-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96f5b-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="96f5b-107">SPNWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96f5b-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="96f5b-108">SPNWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96f5b-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="96f5b-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96f5b-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="96f5b-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96f5b-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96f5b-111">DESCRIPTION</span></span>
<span data-ttu-id="96f5b-112">Das New-AzADSpCredential cmdlet kann zum Hinzufügen neuer Anmeldeinformationen oder zum Rollup der Anmeldeinformationen für einen Dienstprinzipal verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="96f5b-112">The New-AzADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="96f5b-113">Der Dienstprinzipal wird durch Angabe der Objekt-ID oder des Dienstprinzipalnamens identifiziert.</span><span class="sxs-lookup"><span data-stu-id="96f5b-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="96f5b-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="96f5b-114">EXAMPLES</span></span>

### <span data-ttu-id="96f5b-115">Beispiel 1: Erstellen neuer Anmeldeinformationen für den Dienstprinzipal mithilfe eines generierten Kennworts</span><span class="sxs-lookup"><span data-stu-id="96f5b-115">Example 1: Create a new service principal credential using a generated password</span></span>

```powershell
PS C:\> New-AzADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="96f5b-116">Dem vorhandenen Dienstprinzipal wird ein neues Kennwort mit der Objekt-ID '1f99cf81-0146-4f4e-beae-2007d0668476' hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="96f5b-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="96f5b-117">Beispiel 2: Erstellen neuer Anmeldeinformationen für den Dienstprinzipal mithilfe eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="96f5b-117">Example 2: Create a new service principal credential using a certificate</span></span>

```powershell
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="96f5b-118">Das bereitgestellte base64-codierte öffentliche X509-Zertifikat ("myapp.cer") wird dem vorhandenen Dienstprinzipal mithilfe des SPN hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="96f5b-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="96f5b-119">Beispiel 3: Erstellen neuer Anmeldeinformationen für den Dienstprinzipal mithilfe der Piping</span><span class="sxs-lookup"><span data-stu-id="96f5b-119">Example 3: Create a new service principal credential using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="96f5b-120">Ruft den Dienstprinzipal mit der Objekt-ID '1f99cf81-0146-4f4e-beae-2007d0668476' ab und gibt diese an die New-AzADSpCredential weiter, um eine neue Dienstprinzipalanmeldeinformationen für diesen Dienstprinzipal mit einem generierten Kennwort zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="96f5b-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="96f5b-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96f5b-121">PARAMETERS</span></span>

### <span data-ttu-id="96f5b-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="96f5b-122">-CertValue</span></span>
<span data-ttu-id="96f5b-123">Der Wert des "asymmetrischen" Anmeldeinformationstyps.</span><span class="sxs-lookup"><span data-stu-id="96f5b-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="96f5b-124">Es stellt das 64-codierte Basiszertifikat dar.</span><span class="sxs-lookup"><span data-stu-id="96f5b-124">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithCertValueParameterSet, SPNWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96f5b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96f5b-125">-DefaultProfile</span></span>
<span data-ttu-id="96f5b-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="96f5b-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96f5b-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="96f5b-127">-EndDate</span></span>
<span data-ttu-id="96f5b-128">Das Effektive Enddatum der Verwendung der Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="96f5b-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="96f5b-129">Der Standardmäßige Enddatumswert liegt ein Jahr nach heute.</span><span class="sxs-lookup"><span data-stu-id="96f5b-129">The default end date value is one year from today.</span></span>
<span data-ttu-id="96f5b-130">Bei Anmeldeinformationen vom Typ "asymmetrischer Art" muss dies auf das Datum oder vor dem Datum festgelegt werden, an dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="96f5b-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96f5b-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="96f5b-131">-ObjectId</span></span>
<span data-ttu-id="96f5b-132">Die Objekt-ID des Dienstprinzipal, dem die Anmeldeinformationen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="96f5b-132">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96f5b-133">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="96f5b-133">-ServicePrincipalName</span></span>
<span data-ttu-id="96f5b-134">Der Name (SPN) des Dienstprinzipal, dem die Anmeldeinformationen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="96f5b-134">The name (SPN) of the service principal to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithCertValueParameterSet, SPNWithPasswordParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96f5b-135">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="96f5b-135">-ServicePrincipalObject</span></span>
<span data-ttu-id="96f5b-136">Das Dienstprinzipalobjekt, dem die Anmeldeinformationen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="96f5b-136">The service principal object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet, ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96f5b-137">-StartDate</span><span class="sxs-lookup"><span data-stu-id="96f5b-137">-StartDate</span></span>
<span data-ttu-id="96f5b-138">Das Effektive Startdatum der Nutzung der Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="96f5b-138">The effective start date of the credential usage.</span></span>
<span data-ttu-id="96f5b-139">Der Standardwert für das Startdatum ist "Heute".</span><span class="sxs-lookup"><span data-stu-id="96f5b-139">The default start date value is today.</span></span>
<span data-ttu-id="96f5b-140">Bei Anmeldeinformationen vom Typ "asymmetrischer Art" muss dies auf das Datum oder nach dem Datum festgelegt werden, ab dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="96f5b-140">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96f5b-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96f5b-141">-Confirm</span></span>
<span data-ttu-id="96f5b-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="96f5b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96f5b-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="96f5b-143">-WhatIf</span></span>
<span data-ttu-id="96f5b-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="96f5b-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96f5b-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="96f5b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96f5b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96f5b-146">CommonParameters</span></span>
<span data-ttu-id="96f5b-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96f5b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96f5b-148">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96f5b-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96f5b-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="96f5b-149">INPUTS</span></span>

### <span data-ttu-id="96f5b-150">System.String</span><span class="sxs-lookup"><span data-stu-id="96f5b-150">System.String</span></span>

### <span data-ttu-id="96f5b-151">Microsoft.Azure.Commands.ActiveDirectory.WAHLDServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="96f5b-151">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="96f5b-152">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="96f5b-152">System.DateTime</span></span>

## <span data-ttu-id="96f5b-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="96f5b-153">OUTPUTS</span></span>

### <span data-ttu-id="96f5b-154">Microsoft.Azure.Commands.ActiveDirectory.WERDENDCredential</span><span class="sxs-lookup"><span data-stu-id="96f5b-154">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="96f5b-155">Microsoft.Azure.Commands.Resources.Models.Authorization.STARBDCredentialWrapper</span><span class="sxs-lookup"><span data-stu-id="96f5b-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="96f5b-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="96f5b-156">NOTES</span></span>

## <span data-ttu-id="96f5b-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="96f5b-157">RELATED LINKS</span></span>

[<span data-ttu-id="96f5b-158">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="96f5b-158">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="96f5b-159">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="96f5b-159">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="96f5b-160">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="96f5b-160">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)



