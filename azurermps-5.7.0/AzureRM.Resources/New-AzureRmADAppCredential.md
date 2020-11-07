---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
ms.openlocfilehash: d4d7cb0a188b4c00c4ea0c07140b3360c98805aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663434"
---
# <span data-ttu-id="c7d09-101">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c7d09-101">New-AzureRmADAppCredential</span></span>

## <span data-ttu-id="c7d09-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c7d09-102">SYNOPSIS</span></span>
<span data-ttu-id="c7d09-103">Fügt eine Anmeldeinformationen zu einer vorhandenen Anwendung hinzu.</span><span class="sxs-lookup"><span data-stu-id="c7d09-103">Adds a credential to an existing application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7d09-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7d09-104">SYNTAX</span></span>

### <span data-ttu-id="c7d09-105">ApplicationObjectIdWithPasswordParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c7d09-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7d09-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7d09-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7d09-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7d09-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7d09-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7d09-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7d09-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7d09-109">DESCRIPTION</span></span>
<span data-ttu-id="c7d09-110">Mithilfe des New-AzureRmADAppCredential-Cmdlets können Sie eine neue Anmeldeinformationen hinzufügen oder die Anmeldeinformationen für eine Anwendung Rollen.</span><span class="sxs-lookup"><span data-stu-id="c7d09-110">The New-AzureRmADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="c7d09-111">Die Anwendung wird identifiziert, indem entweder die Anwendungsobjekt-ID oder die Anwendungs-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c7d09-111">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="c7d09-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7d09-112">EXAMPLES</span></span>

### <span data-ttu-id="c7d09-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c7d09-113">Example 1</span></span>
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS E:\> New-AzureRmADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="c7d09-114">Eine neue kennwortberechtigung wird einer vorhandenen Anwendung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c7d09-114">A new password credential is added to an existing application.</span></span>
<span data-ttu-id="c7d09-115">In diesem Beispiel wird der angegebene Kennwortwert der Anwendung unter Verwendung der Application-Objekt-ID hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c7d09-115">In this example, the supplied password value is added to the application using the application object id.</span></span>

### <span data-ttu-id="c7d09-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c7d09-116">Example 2</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="c7d09-117">Eine neue Schlüssel Berechtigung wird einer vorhandenen Anwendung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c7d09-117">A new key credential is added to an existing application.</span></span>
<span data-ttu-id="c7d09-118">In diesem Beispiel wird das bereitgestellte Base64-codierte öffentliche X509-Zertifikat ("MyApp. cer") der Anwendung mithilfe von ApplicationId hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c7d09-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the application using the applicationId.</span></span>

### <span data-ttu-id="c7d09-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c7d09-119">Example 3</span></span>
```
PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue
```

## <span data-ttu-id="c7d09-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7d09-120">PARAMETERS</span></span>

### <span data-ttu-id="c7d09-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c7d09-121">-ApplicationId</span></span>
<span data-ttu-id="c7d09-122">Die ID der Anwendung, der die Anmeldeinformationen hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c7d09-122">The id of the application to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d09-123">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="c7d09-123">-CertValue</span></span>
<span data-ttu-id="c7d09-124">Der Wert des Anmeldeinformationstyps "asymmetrisch".</span><span class="sxs-lookup"><span data-stu-id="c7d09-124">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="c7d09-125">Es stellt das Basis 64-codierte Zertifikat dar.</span><span class="sxs-lookup"><span data-stu-id="c7d09-125">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithCertValueParameterSet, ApplicationIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d09-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7d09-126">-DefaultProfile</span></span>
<span data-ttu-id="c7d09-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c7d09-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7d09-128">-Enddate</span><span class="sxs-lookup"><span data-stu-id="c7d09-128">-EndDate</span></span>
<span data-ttu-id="c7d09-129">Das effektive Enddatum der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="c7d09-129">The effective end date of the credential usage.</span></span>
<span data-ttu-id="c7d09-130">Der Standardwert für Enddatum beträgt ein Jahr ab heute.</span><span class="sxs-lookup"><span data-stu-id="c7d09-130">The default end date value is one year from today.</span></span> <span data-ttu-id="c7d09-131">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder vor dem Datum festgesetzt werden, an dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="c7d09-131">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="c7d09-132">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="c7d09-132">-ObjectId</span></span>
<span data-ttu-id="c7d09-133">Die Objekt-ID der Anwendung, der die Anmeldeinformationen hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c7d09-133">The object id of the application to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationObjectIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d09-134">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="c7d09-134">-Password</span></span>
<span data-ttu-id="c7d09-135">Das Kennwort, das der Anwendung zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7d09-135">The password to be associated with the application.</span></span>

```yaml
Type: SecureString
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d09-136">-StartDate</span><span class="sxs-lookup"><span data-stu-id="c7d09-136">-StartDate</span></span>
<span data-ttu-id="c7d09-137">Der effektive Anfangstermin der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="c7d09-137">The effective start date of the credential usage.</span></span>
<span data-ttu-id="c7d09-138">Der Standardwert für das Anfangsdatum ist heute.</span><span class="sxs-lookup"><span data-stu-id="c7d09-138">The default start date value is today.</span></span>
<span data-ttu-id="c7d09-139">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder nach dem Datum festgesetzt werden, ab dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="c7d09-139">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="c7d09-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c7d09-140">-Confirm</span></span>
<span data-ttu-id="c7d09-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c7d09-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7d09-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7d09-142">-WhatIf</span></span>
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

### <span data-ttu-id="c7d09-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7d09-143">CommonParameters</span></span>
<span data-ttu-id="c7d09-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7d09-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7d09-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7d09-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7d09-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c7d09-146">INPUTS</span></span>

### <span data-ttu-id="c7d09-147">Keine</span><span class="sxs-lookup"><span data-stu-id="c7d09-147">None</span></span>
<span data-ttu-id="c7d09-148">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="c7d09-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7d09-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c7d09-149">OUTPUTS</span></span>

### <span data-ttu-id="c7d09-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="c7d09-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="c7d09-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="c7d09-151">NOTES</span></span>

## <span data-ttu-id="c7d09-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c7d09-152">RELATED LINKS</span></span>

[<span data-ttu-id="c7d09-153">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c7d09-153">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="c7d09-154">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c7d09-154">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="c7d09-155">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="c7d09-155">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

