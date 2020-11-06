---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
ms.openlocfilehash: ca338fd648010b9158a6bc308bb4dcb2f1c48317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500414"
---
# <span data-ttu-id="a4929-101">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a4929-101">New-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="a4929-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a4929-102">SYNOPSIS</span></span>
<span data-ttu-id="a4929-103">Erstellt einen neuen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="a4929-103">Creates a new azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4929-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4929-104">SYNTAX</span></span>

### <span data-ttu-id="a4929-105">ApplicationWithoutCredentialParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a4929-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4929-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4929-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4929-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4929-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4929-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4929-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4929-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4929-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4929-110">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4929-110">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4929-111">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4929-111">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4929-112">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4929-112">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4929-113">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4929-113">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4929-114">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4929-114">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4929-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4929-115">DESCRIPTION</span></span>
<span data-ttu-id="a4929-116">Erstellt einen neuen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="a4929-116">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="a4929-117">Hinweis: das Cmdlet erstellt auch implizit eine Anwendung und legt deren Eigenschaften fest (wenn die ApplicationId nicht bereitgestellt wird).</span><span class="sxs-lookup"><span data-stu-id="a4929-117">Note: The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span>
<span data-ttu-id="a4929-118">Verwenden Sie Set-AzureRmADApplication-Cmdlet, um die anwendungsspezifischen Parameter zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a4929-118">In order to update the application specific parameters please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="a4929-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a4929-119">EXAMPLES</span></span>

### <span data-ttu-id="a4929-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a4929-120">Example 1</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
```

<span data-ttu-id="a4929-121">Erstellt einen neuen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="a4929-121">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="a4929-122">DisplayName-Typ-ObjectID</span><span class="sxs-lookup"><span data-stu-id="a4929-122">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="a4929-123">DemoApp ServicePrincipal f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span><span class="sxs-lookup"><span data-stu-id="a4929-123">DemoApp                        ServicePrincipal               f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span></span>

### <span data-ttu-id="a4929-124">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a4929-124">Example 2</span></span>
```
$SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
New-AzureRmADServicePrincipal -DisplayName SPForNoExistingApp -Password $SecureStringPassword
```

<span data-ttu-id="a4929-125">Erstellt einen neuen Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="a4929-125">Creates a new service principal.</span></span>
<span data-ttu-id="a4929-126">Das Cmdlet erstellt auch implizit eine Anwendung, da eine Anwendung nicht bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a4929-126">The cmdlet also implicitly creates an application since one is not provided.</span></span>

<span data-ttu-id="a4929-127">DisplayName-Typ-ObjectID</span><span class="sxs-lookup"><span data-stu-id="a4929-127">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="a4929-128">SPForNoExistingApp ServicePrincipal 784136ca-3ae2-4fdd-a388-89d993e7c780</span><span class="sxs-lookup"><span data-stu-id="a4929-128">SPForNoExistingApp             ServicePrincipal               784136ca-3ae2-4fdd-a388-89d993e7c780</span></span>

## <span data-ttu-id="a4929-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4929-129">PARAMETERS</span></span>

### <span data-ttu-id="a4929-130">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a4929-130">-ApplicationId</span></span>
<span data-ttu-id="a4929-131">Die eindeutige Anwendungs-ID für einen Dienstprinzipal in einem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="a4929-131">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="a4929-132">Nach der Erstellung kann diese Eigenschaft nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a4929-132">Once created this property cannot be changed.</span></span>
<span data-ttu-id="a4929-133">Wenn keine Anwendungs-ID angegeben wird, wird eine Anwendung generiert.</span><span class="sxs-lookup"><span data-stu-id="a4929-133">If an application id is not specified, one will be generated.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4929-134">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="a4929-134">-CertValue</span></span>
<span data-ttu-id="a4929-135">Der Wert des Anmeldeinformationstyps "asymmetrisch".</span><span class="sxs-lookup"><span data-stu-id="a4929-135">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="a4929-136">Es stellt das Basis 64-codierte Zertifikat dar.</span><span class="sxs-lookup"><span data-stu-id="a4929-136">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4929-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4929-137">-DefaultProfile</span></span>
<span data-ttu-id="a4929-138">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a4929-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4929-139">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a4929-139">-DisplayName</span></span>
<span data-ttu-id="a4929-140">Der Anzeigename des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="a4929-140">The friendly name of the service principal.</span></span>

```yaml
Type: String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4929-141">-Enddate</span><span class="sxs-lookup"><span data-stu-id="a4929-141">-EndDate</span></span>
<span data-ttu-id="a4929-142">Das effektive Enddatum der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="a4929-142">The effective end date of the credential usage.</span></span>
<span data-ttu-id="a4929-143">Der Standardwert für Enddatum beträgt ein Jahr ab heute.</span><span class="sxs-lookup"><span data-stu-id="a4929-143">The default end date value is one year from today.</span></span> <span data-ttu-id="a4929-144">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder vor dem Datum festgesetzt werden, an dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="a4929-144">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4929-145">-Keycredentials</span><span class="sxs-lookup"><span data-stu-id="a4929-145">-KeyCredentials</span></span>
<span data-ttu-id="a4929-146">Die Liste der Zertifikatanmeldeinformationen, die dem Dienstprinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a4929-146">The list of certificate credentials associated with the service principal.</span></span>

```yaml
Type: PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4929-147">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="a4929-147">-Password</span></span>
<span data-ttu-id="a4929-148">Das Kennwort, das dem Dienstprinzipal zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4929-148">The password to be associated with the service principal.</span></span>

```yaml
Type: SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4929-149">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="a4929-149">-PasswordCredentials</span></span>
<span data-ttu-id="a4929-150">Die Liste der Kennwortanmeldeinformationen, die dem Dienstprinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a4929-150">The list of password credentials associated with the service principal.</span></span>

```yaml
Type: PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4929-151">-StartDate</span><span class="sxs-lookup"><span data-stu-id="a4929-151">-StartDate</span></span>
<span data-ttu-id="a4929-152">Der effektive Anfangstermin der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="a4929-152">The effective start date of the credential usage.</span></span>
<span data-ttu-id="a4929-153">Der Standardwert für das Anfangsdatum ist heute.</span><span class="sxs-lookup"><span data-stu-id="a4929-153">The default start date value is today.</span></span> <span data-ttu-id="a4929-154">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder nach dem Datum festgesetzt werden, ab dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="a4929-154">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4929-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a4929-155">-Confirm</span></span>
<span data-ttu-id="a4929-156">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a4929-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4929-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4929-157">-WhatIf</span></span>
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

### <span data-ttu-id="a4929-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4929-158">CommonParameters</span></span>
<span data-ttu-id="a4929-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4929-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4929-160">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4929-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4929-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a4929-161">INPUTS</span></span>

### <span data-ttu-id="a4929-162">Keine</span><span class="sxs-lookup"><span data-stu-id="a4929-162">None</span></span>
<span data-ttu-id="a4929-163">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="a4929-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a4929-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a4929-164">OUTPUTS</span></span>

### <span data-ttu-id="a4929-165">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a4929-165">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="a4929-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="a4929-166">NOTES</span></span>
<span data-ttu-id="a4929-167">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="a4929-167">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="a4929-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a4929-168">RELATED LINKS</span></span>

[<span data-ttu-id="a4929-169">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a4929-169">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="a4929-170">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a4929-170">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="a4929-171">Neu – AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="a4929-171">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="a4929-172">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="a4929-172">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="a4929-173">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a4929-173">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="a4929-174">Neu – AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a4929-174">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="a4929-175">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a4929-175">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

