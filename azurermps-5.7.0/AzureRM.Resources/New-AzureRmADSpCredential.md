---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
ms.openlocfilehash: bf2a42df42a343d9745cb55f4d72463513b44dc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498857"
---
# <span data-ttu-id="85a58-101">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="85a58-101">New-AzureRmADSpCredential</span></span>

## <span data-ttu-id="85a58-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="85a58-102">SYNOPSIS</span></span>
<span data-ttu-id="85a58-103">Fügt einem vorhandenen Dienstprinzipal eine Anmeldeinformationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="85a58-103">Adds a credential to an existing service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85a58-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="85a58-104">SYNTAX</span></span>

### <span data-ttu-id="85a58-105">SpObjectIdWithPasswordParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="85a58-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85a58-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="85a58-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85a58-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="85a58-107">SPNWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85a58-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="85a58-108">SPNWithPasswordParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85a58-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85a58-109">DESCRIPTION</span></span>
<span data-ttu-id="85a58-110">Das New-AzureRmADSpCredential-Cmdlet kann verwendet werden, um eine neue Anmeldeinformationen hinzuzufügen oder die Anmeldeinformationen für einen Dienstprinzipal zu Rollen.</span><span class="sxs-lookup"><span data-stu-id="85a58-110">The New-AzureRmADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="85a58-111">Der Dienstprinzipal wird identifiziert, indem entweder die Objekt-ID oder der Dienstprinzipalname angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="85a58-111">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="85a58-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="85a58-112">EXAMPLES</span></span>

### <span data-ttu-id="85a58-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="85a58-113">Example 1</span></span>
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS E:\> New-AzureRmADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $SecureStringPassword
```

<span data-ttu-id="85a58-114">Ein neues Kennwort wird einem vorhandenen Dienstprinzipal hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="85a58-114">A new password credential is added to an existing service principal.</span></span>
<span data-ttu-id="85a58-115">In diesem Beispiel wird der angegebene Kennwortwert dem Dienstprinzipal mithilfe der ObjectID hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="85a58-115">In this example, the supplied password value is added to the service principal using the objectId.</span></span>

### <span data-ttu-id="85a58-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="85a58-116">Example 2</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="85a58-117">Ein neuer Schlüssel Anmeldeinformationen wird einem vorhandenen Dienstprinzipal hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="85a58-117">A new key credential is added to an existing service principal.</span></span>
<span data-ttu-id="85a58-118">In diesem Beispiel wird das bereitgestellte Base64-codierte öffentliche X509-Zertifikat ("MyApp. cer") dem Dienstprinzipal mithilfe seines SPN hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="85a58-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the service principal using its SPN.</span></span>

### <span data-ttu-id="85a58-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="85a58-119">Example 3</span></span>

```
PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue
```

## <span data-ttu-id="85a58-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="85a58-120">PARAMETERS</span></span>

### <span data-ttu-id="85a58-121">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="85a58-121">-CertValue</span></span>
<span data-ttu-id="85a58-122">Der Wert des Anmeldeinformationstyps "asymmetrisch".</span><span class="sxs-lookup"><span data-stu-id="85a58-122">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="85a58-123">Es stellt das Basis 64-codierte Zertifikat dar.</span><span class="sxs-lookup"><span data-stu-id="85a58-123">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithCertValueParameterSet, SPNWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85a58-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85a58-124">-DefaultProfile</span></span>
<span data-ttu-id="85a58-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="85a58-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85a58-126">-Enddate</span><span class="sxs-lookup"><span data-stu-id="85a58-126">-EndDate</span></span>
<span data-ttu-id="85a58-127">Das effektive Enddatum der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="85a58-127">The effective end date of the credential usage.</span></span>
<span data-ttu-id="85a58-128">Der Standardwert für Enddatum beträgt ein Jahr ab heute.</span><span class="sxs-lookup"><span data-stu-id="85a58-128">The default end date value is one year from today.</span></span> <span data-ttu-id="85a58-129">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder vor dem Datum festgesetzt werden, an dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="85a58-129">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85a58-130">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="85a58-130">-ObjectId</span></span>
<span data-ttu-id="85a58-131">Die Objekt-ID des Dienst Prinzipals, dem die Anmeldeinformationen hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="85a58-131">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85a58-132">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="85a58-132">-Password</span></span>
<span data-ttu-id="85a58-133">Das Kennwort, das der Anwendung zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="85a58-133">The password to be associated with the application.</span></span>

```yaml
Type: SecureString
Parameter Sets: SpObjectIdWithPasswordParameterSet, SPNWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85a58-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="85a58-134">-ServicePrincipalName</span></span>
<span data-ttu-id="85a58-135">Der Name (SPN) des Dienst Prinzipals, dem die Anmeldeinformationen hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="85a58-135">The name (SPN) of the service principal to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: SPNWithCertValueParameterSet, SPNWithPasswordParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85a58-136">-StartDate</span><span class="sxs-lookup"><span data-stu-id="85a58-136">-StartDate</span></span>
<span data-ttu-id="85a58-137">Der effektive Anfangstermin der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="85a58-137">The effective start date of the credential usage.</span></span>
<span data-ttu-id="85a58-138">Der Standardwert für das Anfangsdatum ist heute.</span><span class="sxs-lookup"><span data-stu-id="85a58-138">The default start date value is today.</span></span> <span data-ttu-id="85a58-139">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder nach dem Datum festgesetzt werden, ab dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="85a58-139">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85a58-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="85a58-140">-Confirm</span></span>
<span data-ttu-id="85a58-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="85a58-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85a58-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85a58-142">-WhatIf</span></span>
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

### <span data-ttu-id="85a58-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85a58-143">CommonParameters</span></span>
<span data-ttu-id="85a58-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85a58-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85a58-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85a58-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85a58-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="85a58-146">INPUTS</span></span>

### <span data-ttu-id="85a58-147">Keine</span><span class="sxs-lookup"><span data-stu-id="85a58-147">None</span></span>
<span data-ttu-id="85a58-148">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="85a58-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="85a58-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="85a58-149">OUTPUTS</span></span>

### <span data-ttu-id="85a58-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="85a58-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="85a58-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="85a58-151">NOTES</span></span>

## <span data-ttu-id="85a58-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="85a58-152">RELATED LINKS</span></span>

[<span data-ttu-id="85a58-153">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="85a58-153">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="85a58-154">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="85a58-154">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="85a58-155">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="85a58-155">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



