---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultcertificateorganizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
ms.openlocfilehash: ee2be43882eb434d8bbc533e0d10722f63427a83
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944092"
---
# <span data-ttu-id="8173f-101">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="8173f-101">New-AzKeyVaultCertificateOrganizationDetail</span></span>

## <span data-ttu-id="8173f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8173f-102">SYNOPSIS</span></span>
<span data-ttu-id="8173f-103">Erstellt ein Detailobjekt der Speicherzertifikatorganisation.</span><span class="sxs-lookup"><span data-stu-id="8173f-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="8173f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8173f-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetail [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8173f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8173f-105">DESCRIPTION</span></span>
<span data-ttu-id="8173f-106">Das **Cmdlet New-AzKeyVaultCertificateOrganizationDetail** erstellt ein Detailobjekt der Speicherzertifikatorganisation.</span><span class="sxs-lookup"><span data-stu-id="8173f-106">The **New-AzKeyVaultCertificateOrganizationDetail** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="8173f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8173f-107">EXAMPLES</span></span>

### <span data-ttu-id="8173f-108">Beispiel 1: Erstellen eines Organisationsdetailses</span><span class="sxs-lookup"><span data-stu-id="8173f-108">Example 1: Create an organization details object</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails

Id AdministratorDetails
-- --------------------
   {Patti}
```

<span data-ttu-id="8173f-109">Mit dem ersten Befehl wird ein Detailobjekt des Zertifikatadministrators erstellt und dann in der $AdminDetails gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8173f-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>
<span data-ttu-id="8173f-110">Mit dem zweiten Befehl wird ein Detailobjekt der Zertifikatorganisation erstellt und dann in der $OrgDetails gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8173f-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="8173f-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8173f-111">PARAMETERS</span></span>

### <span data-ttu-id="8173f-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="8173f-112">-AdministratorDetails</span></span>
<span data-ttu-id="8173f-113">Gibt die Zertifikatorganisationsadministratoren an.</span><span class="sxs-lookup"><span data-stu-id="8173f-113">Specifies the certificate organization administrators.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8173f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8173f-114">-DefaultProfile</span></span>
<span data-ttu-id="8173f-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8173f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8173f-116">-ID</span><span class="sxs-lookup"><span data-stu-id="8173f-116">-Id</span></span>
<span data-ttu-id="8173f-117">Gibt den Bezeichner für die Organisation an.</span><span class="sxs-lookup"><span data-stu-id="8173f-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="8173f-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8173f-118">-Confirm</span></span>
<span data-ttu-id="8173f-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8173f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8173f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8173f-120">-WhatIf</span></span>
<span data-ttu-id="8173f-121">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8173f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8173f-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8173f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8173f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8173f-123">CommonParameters</span></span>
<span data-ttu-id="8173f-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8173f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8173f-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8173f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8173f-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8173f-126">INPUTS</span></span>

### <span data-ttu-id="8173f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="8173f-127">System.String</span></span>

### <span data-ttu-id="8173f-128">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="8173f-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8173f-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8173f-129">OUTPUTS</span></span>

### <span data-ttu-id="8173f-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="8173f-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="8173f-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8173f-131">NOTES</span></span>

## <span data-ttu-id="8173f-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8173f-132">RELATED LINKS</span></span>

[<span data-ttu-id="8173f-133">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="8173f-133">New-AzKeyVaultCertificateAdministratorDetail</span></span>](./New-AzKeyVaultCertificateAdministratorDetail.md)

