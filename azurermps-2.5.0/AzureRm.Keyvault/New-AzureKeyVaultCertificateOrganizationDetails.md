---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateorganizationdetails
schema: 2.0.0
ms.openlocfilehash: 76e0d37ac38c8b9799093ff3a4f4ea10c2fce2f4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849992"
---
# <span data-ttu-id="1ac8d-101">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="1ac8d-101">New-AzureKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="1ac8d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1ac8d-102">SYNOPSIS</span></span>
<span data-ttu-id="1ac8d-103">Erstellt ein Objekt im Arbeitsspeicher Zertifikat Organisation Details.</span><span class="sxs-lookup"><span data-stu-id="1ac8d-103">Creates an in-memory certificate organization details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ac8d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ac8d-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateOrganizationDetails [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ac8d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ac8d-105">DESCRIPTION</span></span>
<span data-ttu-id="1ac8d-106">Mit dem Cmdlet " **New-AzureKeyVaultCertificateOrganizationDetails** " wird ein Zertifikat Organisationsdetails-Objekt im Arbeitsspeicher erstellt.</span><span class="sxs-lookup"><span data-stu-id="1ac8d-106">The **New-AzureKeyVaultCertificateOrganizationDetails** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="1ac8d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ac8d-107">EXAMPLES</span></span>

### <span data-ttu-id="1ac8d-108">Beispiel 1: Erstellen eines Organisationsdetails-Objekts</span><span class="sxs-lookup"><span data-stu-id="1ac8d-108">Example 1: Create an organization details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
$OrgDetails = New-AzureKeyVaultCertificateOrganizationDetails -Name "Contoso" -Address1 "1 Redmond Way" -Address2 "Suite 906" -City "Redmond" -State "WA" -Zip 98052 -Country "US" -AdministratorDetails $AdminDetails
```

<span data-ttu-id="1ac8d-109">Der erste Befehl erstellt ein Zertifikat Administrator Details-Objekt und speichert es dann in der $AdminDetails-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1ac8d-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

<span data-ttu-id="1ac8d-110">Mit dem zweiten Befehl wird ein Objekt für die Zertifikats Organisation Details erstellt und dann in der $OrgDetails-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1ac8d-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="1ac8d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ac8d-111">PARAMETERS</span></span>

### <span data-ttu-id="1ac8d-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="1ac8d-112">-AdministratorDetails</span></span>
<span data-ttu-id="1ac8d-113">Gibt die Zertifikat Organisationsadministratoren an.</span><span class="sxs-lookup"><span data-stu-id="1ac8d-113">Specifies the certificate organization administrators.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac8d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ac8d-114">-DefaultProfile</span></span>
<span data-ttu-id="1ac8d-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1ac8d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ac8d-116">-ID</span><span class="sxs-lookup"><span data-stu-id="1ac8d-116">-Id</span></span>
<span data-ttu-id="1ac8d-117">Gibt den Bezeichner für die Organisation an.</span><span class="sxs-lookup"><span data-stu-id="1ac8d-117">Specifies the identifier for the organization.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac8d-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1ac8d-118">-Confirm</span></span>
<span data-ttu-id="1ac8d-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ac8d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ac8d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ac8d-120">-WhatIf</span></span>
<span data-ttu-id="1ac8d-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1ac8d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ac8d-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ac8d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ac8d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ac8d-123">CommonParameters</span></span>
<span data-ttu-id="1ac8d-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ac8d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ac8d-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ac8d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ac8d-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1ac8d-126">INPUTS</span></span>

## <span data-ttu-id="1ac8d-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1ac8d-127">OUTPUTS</span></span>

### <span data-ttu-id="1ac8d-128">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="1ac8d-128">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="1ac8d-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="1ac8d-129">NOTES</span></span>

## <span data-ttu-id="1ac8d-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1ac8d-130">RELATED LINKS</span></span>

[<span data-ttu-id="1ac8d-131">Neu – AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="1ac8d-131">New-AzureKeyVaultCertificateAdministratorDetails</span></span>](./New-AzureKeyVaultCertificateAdministratorDetails.md)

