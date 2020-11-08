---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateorganizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
ms.openlocfilehash: 56b956aa8a65c4586859325f110f3ce593b2289c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180419"
---
# <span data-ttu-id="dedfd-101">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="dedfd-101">New-AzKeyVaultCertificateOrganizationDetail</span></span>

## <span data-ttu-id="dedfd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dedfd-102">SYNOPSIS</span></span>
<span data-ttu-id="dedfd-103">Erstellt ein Objekt im Arbeitsspeicher Zertifikat Organisation Details.</span><span class="sxs-lookup"><span data-stu-id="dedfd-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="dedfd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dedfd-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetail [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dedfd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dedfd-105">DESCRIPTION</span></span>
<span data-ttu-id="dedfd-106">Mit dem Cmdlet " **New-AzKeyVaultCertificateOrganizationDetail** " wird ein Zertifikat Organisationsdetails-Objekt im Arbeitsspeicher erstellt.</span><span class="sxs-lookup"><span data-stu-id="dedfd-106">The **New-AzKeyVaultCertificateOrganizationDetail** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="dedfd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dedfd-107">EXAMPLES</span></span>

### <span data-ttu-id="dedfd-108">Beispiel 1: Erstellen eines Organisationsdetails-Objekts</span><span class="sxs-lookup"><span data-stu-id="dedfd-108">Example 1: Create an organization details object</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails

Id AdministratorDetails
-- --------------------
   {Patti}
```

<span data-ttu-id="dedfd-109">Der erste Befehl erstellt ein Zertifikat Administrator Details-Objekt und speichert es dann in der $AdminDetails-Variablen.</span><span class="sxs-lookup"><span data-stu-id="dedfd-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>
<span data-ttu-id="dedfd-110">Mit dem zweiten Befehl wird ein Objekt für die Zertifikats Organisation Details erstellt und dann in der $OrgDetails-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="dedfd-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="dedfd-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="dedfd-111">PARAMETERS</span></span>

### <span data-ttu-id="dedfd-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="dedfd-112">-AdministratorDetails</span></span>
<span data-ttu-id="dedfd-113">Gibt die Zertifikat Organisationsadministratoren an.</span><span class="sxs-lookup"><span data-stu-id="dedfd-113">Specifies the certificate organization administrators.</span></span>

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

### <span data-ttu-id="dedfd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dedfd-114">-DefaultProfile</span></span>
<span data-ttu-id="dedfd-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="dedfd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dedfd-116">-ID</span><span class="sxs-lookup"><span data-stu-id="dedfd-116">-Id</span></span>
<span data-ttu-id="dedfd-117">Gibt den Bezeichner für die Organisation an.</span><span class="sxs-lookup"><span data-stu-id="dedfd-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="dedfd-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dedfd-118">-Confirm</span></span>
<span data-ttu-id="dedfd-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dedfd-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dedfd-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dedfd-120">-WhatIf</span></span>
<span data-ttu-id="dedfd-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dedfd-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dedfd-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dedfd-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dedfd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dedfd-123">CommonParameters</span></span>
<span data-ttu-id="dedfd-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dedfd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dedfd-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dedfd-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dedfd-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dedfd-126">INPUTS</span></span>

### <span data-ttu-id="dedfd-127">System. String</span><span class="sxs-lookup"><span data-stu-id="dedfd-127">System.String</span></span>

### <span data-ttu-id="dedfd-128">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateAdministratorDetails, Microsoft. Azure. PowerShell. Cmdlets. keyvault, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dedfd-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="dedfd-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dedfd-129">OUTPUTS</span></span>

### <span data-ttu-id="dedfd-130">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="dedfd-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="dedfd-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="dedfd-131">NOTES</span></span>

## <span data-ttu-id="dedfd-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dedfd-132">RELATED LINKS</span></span>

[<span data-ttu-id="dedfd-133">Neu – AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="dedfd-133">New-AzKeyVaultCertificateAdministratorDetail</span></span>](./New-AzKeyVaultCertificateAdministratorDetail.md)

