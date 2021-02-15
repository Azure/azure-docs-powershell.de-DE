---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateadministratordetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
ms.openlocfilehash: 39deb08468912bf727198ec4f90f5f4f0680941f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167249"
---
# <span data-ttu-id="579e1-101">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="579e1-101">New-AzKeyVaultCertificateAdministratorDetail</span></span>

## <span data-ttu-id="579e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="579e1-102">SYNOPSIS</span></span>
<span data-ttu-id="579e1-103">Erstellt ein Speicherzertifikat-Administrator-Detailobjekt.</span><span class="sxs-lookup"><span data-stu-id="579e1-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="579e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="579e1-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="579e1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="579e1-105">DESCRIPTION</span></span>
<span data-ttu-id="579e1-106">Das **Cmdlet "New-AzKeyVaultCertificateAdministratorDetail"** erstellt ein Speicherzertifikat-Administratordetailobjekt.</span><span class="sxs-lookup"><span data-stu-id="579e1-106">The **New-AzKeyVaultCertificateAdministratorDetail** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="579e1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="579e1-107">EXAMPLES</span></span>

### <span data-ttu-id="579e1-108">Beispiel 1: Erstellen eines Detailobjekts für den Zertifikatadministrator</span><span class="sxs-lookup"><span data-stu-id="579e1-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="579e1-109">Mit diesem Befehl wird ein Detailobjekt für den Speicherzertifikatadministrator erstellt und dann in der $AdminDetails gespeichert.</span><span class="sxs-lookup"><span data-stu-id="579e1-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="579e1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="579e1-110">PARAMETERS</span></span>

### <span data-ttu-id="579e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="579e1-111">-DefaultProfile</span></span>
<span data-ttu-id="579e1-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="579e1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="579e1-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="579e1-113">-EmailAddress</span></span>
<span data-ttu-id="579e1-114">Gibt die E-Mail-Adresse für den Zertifikatadministrator an.</span><span class="sxs-lookup"><span data-stu-id="579e1-114">Specifies the email address for the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="579e1-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="579e1-115">-FirstName</span></span>
<span data-ttu-id="579e1-116">Gibt den Vornamen des Zertifikatadministrators an.</span><span class="sxs-lookup"><span data-stu-id="579e1-116">Specifies the first name of the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="579e1-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="579e1-117">-LastName</span></span>
<span data-ttu-id="579e1-118">Gibt den Nachnamen des Zertifikatadministrators an.</span><span class="sxs-lookup"><span data-stu-id="579e1-118">Specifies the last name of the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="579e1-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="579e1-119">-PhoneNumber</span></span>
<span data-ttu-id="579e1-120">Gibt die Telefonnummer des Zertifikatadministrators an.</span><span class="sxs-lookup"><span data-stu-id="579e1-120">Specifies the phone number of the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="579e1-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="579e1-121">-Confirm</span></span>
<span data-ttu-id="579e1-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="579e1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="579e1-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="579e1-123">-WhatIf</span></span>
<span data-ttu-id="579e1-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="579e1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="579e1-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="579e1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="579e1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="579e1-126">CommonParameters</span></span>
<span data-ttu-id="579e1-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="579e1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="579e1-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="579e1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="579e1-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="579e1-129">INPUTS</span></span>

### <span data-ttu-id="579e1-130">System.String</span><span class="sxs-lookup"><span data-stu-id="579e1-130">System.String</span></span>

## <span data-ttu-id="579e1-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="579e1-131">OUTPUTS</span></span>

### <span data-ttu-id="579e1-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="579e1-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="579e1-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="579e1-133">NOTES</span></span>

## <span data-ttu-id="579e1-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="579e1-134">RELATED LINKS</span></span>

[<span data-ttu-id="579e1-135">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="579e1-135">New-AzKeyVaultCertificateOrganizationDetail</span></span>](./New-AzKeyVaultCertificateOrganizationDetail.md)

