---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateadministratordetails
schema: 2.0.0
ms.openlocfilehash: 50da8cae0af437ee86fd7462b285b812368b2508
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849995"
---
# <span data-ttu-id="46f86-101">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="46f86-101">New-AzureKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="46f86-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46f86-102">SYNOPSIS</span></span>
<span data-ttu-id="46f86-103">Erstellt ein Zertifikat Administrator Details-Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="46f86-103">Creates an in-memory certificate administrator details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46f86-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46f86-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46f86-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46f86-105">DESCRIPTION</span></span>
<span data-ttu-id="46f86-106">Mit dem Cmdlet **New-AzureKeyVaultCertificateAdministratorDetails** wird ein speicherresidentes Zertifikat-Administrator Details-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="46f86-106">The **New-AzureKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="46f86-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46f86-107">EXAMPLES</span></span>

### <span data-ttu-id="46f86-108">Beispiel 1: Erstellen eines Zertifikats Administrator Details-Objekts</span><span class="sxs-lookup"><span data-stu-id="46f86-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="46f86-109">Mit diesem Befehl wird ein in-Memory-Zertifikat Administrator Details-Objekt erstellt und dann in der $AdminDetails-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="46f86-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="46f86-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="46f86-110">PARAMETERS</span></span>

### <span data-ttu-id="46f86-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46f86-111">-DefaultProfile</span></span>
<span data-ttu-id="46f86-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="46f86-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46f86-113">-Email-Email</span><span class="sxs-lookup"><span data-stu-id="46f86-113">-EmailAddress</span></span>
<span data-ttu-id="46f86-114">Gibt die e-Mail-Adresse des Zertifikat Administrators an.</span><span class="sxs-lookup"><span data-stu-id="46f86-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="46f86-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="46f86-115">-FirstName</span></span>
<span data-ttu-id="46f86-116">Gibt den Vornamen des Zertifikat Administrators an.</span><span class="sxs-lookup"><span data-stu-id="46f86-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="46f86-117">-Nachname</span><span class="sxs-lookup"><span data-stu-id="46f86-117">-LastName</span></span>
<span data-ttu-id="46f86-118">Gibt den letzten Namen des Zertifikat Administrators an.</span><span class="sxs-lookup"><span data-stu-id="46f86-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="46f86-119">-Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="46f86-119">-PhoneNumber</span></span>
<span data-ttu-id="46f86-120">Gibt die Telefonnummer des Zertifikat Administrators an.</span><span class="sxs-lookup"><span data-stu-id="46f86-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="46f86-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46f86-121">-Confirm</span></span>
<span data-ttu-id="46f86-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46f86-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46f86-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46f86-123">-WhatIf</span></span>
<span data-ttu-id="46f86-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46f86-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46f86-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46f86-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46f86-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46f86-126">CommonParameters</span></span>
<span data-ttu-id="46f86-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46f86-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46f86-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46f86-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46f86-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46f86-129">INPUTS</span></span>

## <span data-ttu-id="46f86-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46f86-130">OUTPUTS</span></span>

### <span data-ttu-id="46f86-131">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="46f86-131">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="46f86-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="46f86-132">NOTES</span></span>

## <span data-ttu-id="46f86-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46f86-133">RELATED LINKS</span></span>

[<span data-ttu-id="46f86-134">Neu – AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="46f86-134">New-AzureKeyVaultCertificateOrganizationDetails</span></span>](./New-AzureKeyVaultCertificateOrganizationDetails.md)

