---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
ms.openlocfilehash: af2eb05e627af1b88948b2c1be0229eb6680254c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659604"
---
# <span data-ttu-id="5e661-101">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5e661-101">New-AzADSpCredential</span></span>

## <span data-ttu-id="5e661-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e661-102">SYNOPSIS</span></span>
<span data-ttu-id="5e661-103">Fügt einem vorhandenen Dienstprinzipal eine Anmeldeinformationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="5e661-103">Adds a credential to an existing service principal.</span></span>

## <span data-ttu-id="5e661-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e661-104">SYNTAX</span></span>

### <span data-ttu-id="5e661-105">SpObjectIdWithPasswordParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e661-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADSpCredential -ObjectId <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e661-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e661-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e661-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e661-107">SPNWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e661-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e661-108">SPNWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e661-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e661-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e661-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e661-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e661-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e661-111">DESCRIPTION</span></span>
<span data-ttu-id="5e661-112">Das New-AzADSpCredential-Cmdlet kann verwendet werden, um eine neue Anmeldeinformationen hinzuzufügen oder die Anmeldeinformationen für einen Dienstprinzipal zu Rollen.</span><span class="sxs-lookup"><span data-stu-id="5e661-112">The New-AzADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="5e661-113">Der Dienstprinzipal wird identifiziert, indem entweder die Objekt-ID oder der Dienstprinzipalname angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5e661-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="5e661-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e661-114">EXAMPLES</span></span>

### <span data-ttu-id="5e661-115">Beispiel 1: Erstellen eines neuen Dienst Prinzipals mit einem generierten Kennwort</span><span class="sxs-lookup"><span data-stu-id="5e661-115">Example 1 - Create a new service principal credential using a generated password</span></span>

```
PS C:\> New-AzADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="5e661-116">Dem vorhandenen Dienstprinzipal wird eine neue kennwortberechtigung mit der Objekt-ID "1f99cf81-0146-4f4e-BEAE-2007d0668476" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5e661-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="5e661-117">Beispiel 2: Erstellen einer neuen Dienstprinzipal Anmeldeinformationen mithilfe eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="5e661-117">Example 2 - Create a new service principal credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="5e661-118">Das bereitgestellte Base64-codierte öffentliche X509-Zertifikat ("MyApp. cer") wird dem vorhandenen Dienstprinzipal mithilfe seines SPN hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5e661-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="5e661-119">Beispiel 3: Erstellen einer neuen Dienstprinzipal Anmeldeinformationen mithilfe von Piping</span><span class="sxs-lookup"><span data-stu-id="5e661-119">Example 3 - Create a new service principal credential using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="5e661-120">Ruft den Dienstprinzipal mit der Objekt-ID "1f99cf81-0146-4f4e-BEAE-2007d0668476" und Pipes ab, die zum New-AzADSpCredential, um eine neue Dienstprinzipal Anmeldeinformationen für diesen Dienstprinzipal mit einem generierten Kennwort zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5e661-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="5e661-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e661-121">PARAMETERS</span></span>

### <span data-ttu-id="5e661-122">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="5e661-122">-CertValue</span></span>
<span data-ttu-id="5e661-123">Der Wert des Anmeldeinformationstyps "asymmetrisch".</span><span class="sxs-lookup"><span data-stu-id="5e661-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="5e661-124">Es stellt das Basis 64-codierte Zertifikat dar.</span><span class="sxs-lookup"><span data-stu-id="5e661-124">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="5e661-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e661-125">-DefaultProfile</span></span>
<span data-ttu-id="5e661-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5e661-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e661-127">-Enddate</span><span class="sxs-lookup"><span data-stu-id="5e661-127">-EndDate</span></span>
<span data-ttu-id="5e661-128">Das effektive Enddatum der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="5e661-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="5e661-129">Der Standardwert für Enddatum beträgt ein Jahr ab heute.</span><span class="sxs-lookup"><span data-stu-id="5e661-129">The default end date value is one year from today.</span></span>
<span data-ttu-id="5e661-130">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder vor dem Datum festgesetzt werden, an dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="5e661-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="5e661-131">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="5e661-131">-ObjectId</span></span>
<span data-ttu-id="5e661-132">Die Objekt-ID des Dienst Prinzipals, dem die Anmeldeinformationen hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5e661-132">The object id of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="5e661-133">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="5e661-133">-ServicePrincipalName</span></span>
<span data-ttu-id="5e661-134">Der Name (SPN) des Dienst Prinzipals, dem die Anmeldeinformationen hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5e661-134">The name (SPN) of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="5e661-135">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="5e661-135">-ServicePrincipalObject</span></span>
<span data-ttu-id="5e661-136">Das Dienstprinzipal Objekt, dem die Anmeldeinformationen hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5e661-136">The service principal object to add the credentials to.</span></span>

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

### <span data-ttu-id="5e661-137">-StartDate</span><span class="sxs-lookup"><span data-stu-id="5e661-137">-StartDate</span></span>
<span data-ttu-id="5e661-138">Der effektive Anfangstermin der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="5e661-138">The effective start date of the credential usage.</span></span>
<span data-ttu-id="5e661-139">Der Standardwert für das Anfangsdatum ist heute.</span><span class="sxs-lookup"><span data-stu-id="5e661-139">The default start date value is today.</span></span>
<span data-ttu-id="5e661-140">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder nach dem Datum festgesetzt werden, ab dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="5e661-140">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="5e661-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5e661-141">-Confirm</span></span>
<span data-ttu-id="5e661-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e661-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e661-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e661-143">-WhatIf</span></span>
<span data-ttu-id="5e661-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e661-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e661-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e661-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e661-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e661-146">CommonParameters</span></span>
<span data-ttu-id="5e661-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e661-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e661-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e661-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e661-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e661-149">INPUTS</span></span>

### <span data-ttu-id="5e661-150">System. String</span><span class="sxs-lookup"><span data-stu-id="5e661-150">System.String</span></span>

### <span data-ttu-id="5e661-151">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5e661-151">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="5e661-152">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="5e661-152">System.DateTime</span></span>

## <span data-ttu-id="5e661-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e661-153">OUTPUTS</span></span>

### <span data-ttu-id="5e661-154">Microsoft. Azure. Commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="5e661-154">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="5e661-155">Microsoft. Azure. Commands. resources. Models. Authorization. PSADCredentialWrapper</span><span class="sxs-lookup"><span data-stu-id="5e661-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="5e661-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e661-156">NOTES</span></span>

## <span data-ttu-id="5e661-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e661-157">RELATED LINKS</span></span>

[<span data-ttu-id="5e661-158">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5e661-158">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="5e661-159">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5e661-159">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="5e661-160">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5e661-160">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)



