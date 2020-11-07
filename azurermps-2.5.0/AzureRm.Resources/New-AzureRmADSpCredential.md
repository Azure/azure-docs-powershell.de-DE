---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadspcredential
schema: 2.0.0
ms.openlocfilehash: 2f4a5e19f9b563361b526fab386c068fe65ce6ca
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850284"
---
# <span data-ttu-id="01971-101">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="01971-101">New-AzureRmADSpCredential</span></span>

## <span data-ttu-id="01971-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="01971-102">SYNOPSIS</span></span>
<span data-ttu-id="01971-103">Fügt einem vorhandenen Dienstprinzipal eine Anmeldeinformationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="01971-103">Adds a credential to an existing service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01971-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="01971-104">SYNTAX</span></span>

### <span data-ttu-id="01971-105">SpObjectIdWithPasswordParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="01971-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADSpCredential -ObjectId <Guid> [-Password <SecureString>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01971-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="01971-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ObjectId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01971-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="01971-107">SPNWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01971-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="01971-108">SPNWithPasswordParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> [-Password <SecureString>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01971-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="01971-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01971-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="01971-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01971-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="01971-111">DESCRIPTION</span></span>
<span data-ttu-id="01971-112">Das New-AzureRmADSpCredential-Cmdlet kann verwendet werden, um eine neue Anmeldeinformationen hinzuzufügen oder die Anmeldeinformationen für einen Dienstprinzipal zu Rollen.</span><span class="sxs-lookup"><span data-stu-id="01971-112">The New-AzureRmADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="01971-113">Der Dienstprinzipal wird identifiziert, indem entweder die Objekt-ID oder der Dienstprinzipalname angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="01971-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="01971-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="01971-114">EXAMPLES</span></span>

### <span data-ttu-id="01971-115">Beispiel 1: Erstellen eines neuen Dienst Prinzipals mit einem generierten Kennwort</span><span class="sxs-lookup"><span data-stu-id="01971-115">Example 1 - Create a new service principal credential using a generated password</span></span>

```
PS C:\> New-AzureRmADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="01971-116">Dem vorhandenen Dienstprinzipal wird eine neue kennwortberechtigung mit der Objekt-ID "1f99cf81-0146-4f4e-BEAE-2007d0668476" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="01971-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="01971-117">Beispiel 2: Erstellen einer neuen Dienstprinzipal Anmeldeinformationen mithilfe eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="01971-117">Example 2 - Create a new service principal credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 
PS C:\> $cer.Import("C:\myapp.cer") 
PS C:\> $binCert = $cer.GetRawCertData() 
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="01971-118">Das bereitgestellte Base64-codierte öffentliche X509-Zertifikat ("MyApp. cer") wird dem vorhandenen Dienstprinzipal mithilfe seines SPN hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="01971-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="01971-119">Beispiel 3: Erstellen einer neuen Dienstprinzipal Anmeldeinformationen mithilfe von Piping</span><span class="sxs-lookup"><span data-stu-id="01971-119">Example 3 - Create a new service principal credential using piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzureRmADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="01971-120">Ruft den Dienstprinzipal mit der Objekt-ID "1f99cf81-0146-4f4e-BEAE-2007d0668476" und Pipes ab, die zum New-AzureRmADSpCredential, um eine neue Dienstprinzipal Anmeldeinformationen für diesen Dienstprinzipal mit einem generierten Kennwort zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="01971-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzureRmADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="01971-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="01971-121">PARAMETERS</span></span>

### <span data-ttu-id="01971-122">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="01971-122">-CertValue</span></span>
<span data-ttu-id="01971-123">Der Wert des Anmeldeinformationstyps "asymmetrisch".</span><span class="sxs-lookup"><span data-stu-id="01971-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="01971-124">Es stellt das Basis 64-codierte Zertifikat dar.</span><span class="sxs-lookup"><span data-stu-id="01971-124">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="01971-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01971-125">-DefaultProfile</span></span>
<span data-ttu-id="01971-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="01971-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01971-127">-Enddate</span><span class="sxs-lookup"><span data-stu-id="01971-127">-EndDate</span></span>
<span data-ttu-id="01971-128">Das effektive Enddatum der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="01971-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="01971-129">Der Standardwert für Enddatum beträgt ein Jahr ab heute.</span><span class="sxs-lookup"><span data-stu-id="01971-129">The default end date value is one year from today.</span></span> <span data-ttu-id="01971-130">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder vor dem Datum festgesetzt werden, an dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="01971-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="01971-131">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="01971-131">-ObjectId</span></span>
<span data-ttu-id="01971-132">Die Objekt-ID des Dienst Prinzipals, dem die Anmeldeinformationen hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="01971-132">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01971-133">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="01971-133">-Password</span></span>
<span data-ttu-id="01971-134">Das Kennwort, das der Anwendung zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="01971-134">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SpObjectIdWithPasswordParameterSet, SPNWithPasswordParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01971-135">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="01971-135">-ServicePrincipalName</span></span>
<span data-ttu-id="01971-136">Der Name (SPN) des Dienst Prinzipals, dem die Anmeldeinformationen hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="01971-136">The name (SPN) of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="01971-137">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="01971-137">-ServicePrincipalObject</span></span>
<span data-ttu-id="01971-138">Das Dienstprinzipal Objekt, dem die Anmeldeinformationen hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="01971-138">The service principal object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet, ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01971-139">-StartDate</span><span class="sxs-lookup"><span data-stu-id="01971-139">-StartDate</span></span>
<span data-ttu-id="01971-140">Der effektive Anfangstermin der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="01971-140">The effective start date of the credential usage.</span></span>
<span data-ttu-id="01971-141">Der Standardwert für das Anfangsdatum ist heute.</span><span class="sxs-lookup"><span data-stu-id="01971-141">The default start date value is today.</span></span> <span data-ttu-id="01971-142">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder nach dem Datum festgesetzt werden, ab dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="01971-142">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="01971-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="01971-143">-Confirm</span></span>
<span data-ttu-id="01971-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="01971-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01971-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01971-145">-WhatIf</span></span>
<span data-ttu-id="01971-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01971-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01971-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01971-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01971-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01971-148">CommonParameters</span></span>
<span data-ttu-id="01971-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01971-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01971-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01971-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01971-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="01971-151">INPUTS</span></span>

### <span data-ttu-id="01971-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="01971-152">System.Guid</span></span>

### <span data-ttu-id="01971-153">System. String</span><span class="sxs-lookup"><span data-stu-id="01971-153">System.String</span></span>

### <span data-ttu-id="01971-154">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="01971-154">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="01971-155">Parameter: ServicePrincipalObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="01971-155">Parameters: ServicePrincipalObject (ByValue)</span></span>

### <span data-ttu-id="01971-156">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="01971-156">System.Security.SecureString</span></span>

### <span data-ttu-id="01971-157">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="01971-157">System.DateTime</span></span>

## <span data-ttu-id="01971-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="01971-158">OUTPUTS</span></span>

### <span data-ttu-id="01971-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="01971-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="01971-160">Microsoft. Azure. Commands. resources. Models. Authorization. PSADCredentialWrapper</span><span class="sxs-lookup"><span data-stu-id="01971-160">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="01971-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="01971-161">NOTES</span></span>

## <span data-ttu-id="01971-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="01971-162">RELATED LINKS</span></span>

[<span data-ttu-id="01971-163">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="01971-163">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="01971-164">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="01971-164">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="01971-165">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="01971-165">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



