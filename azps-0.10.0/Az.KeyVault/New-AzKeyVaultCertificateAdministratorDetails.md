---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-AzKeyvaultcertificateadministratordetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetails.md
ms.openlocfilehash: 6844a8f4858452a1ebf9df306d75e495603703aa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842131"
---
# <span data-ttu-id="07ada-101">New-AzKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="07ada-101">New-AzKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="07ada-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07ada-102">SYNOPSIS</span></span>
<span data-ttu-id="07ada-103">Erstellt ein Zertifikat Administrator Details-Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="07ada-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="07ada-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="07ada-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07ada-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07ada-105">DESCRIPTION</span></span>
<span data-ttu-id="07ada-106">Mit dem Cmdlet **New-AzKeyVaultCertificateAdministratorDetails** wird ein speicherresidentes Zertifikat-Administrator Details-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="07ada-106">The **New-AzKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="07ada-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07ada-107">EXAMPLES</span></span>

### <span data-ttu-id="07ada-108">Beispiel 1: Erstellen eines Zertifikats Administrator Details-Objekts</span><span class="sxs-lookup"><span data-stu-id="07ada-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="07ada-109">Mit diesem Befehl wird ein in-Memory-Zertifikat Administrator Details-Objekt erstellt und dann in der $AdminDetails-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="07ada-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="07ada-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="07ada-110">PARAMETERS</span></span>

### <span data-ttu-id="07ada-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07ada-111">-DefaultProfile</span></span>
<span data-ttu-id="07ada-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="07ada-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ada-113">-Email-Email</span><span class="sxs-lookup"><span data-stu-id="07ada-113">-EmailAddress</span></span>
<span data-ttu-id="07ada-114">Gibt die e-Mail-Adresse des Zertifikat Administrators an.</span><span class="sxs-lookup"><span data-stu-id="07ada-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="07ada-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="07ada-115">-FirstName</span></span>
<span data-ttu-id="07ada-116">Gibt den Vornamen des Zertifikat Administrators an.</span><span class="sxs-lookup"><span data-stu-id="07ada-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="07ada-117">-Nachname</span><span class="sxs-lookup"><span data-stu-id="07ada-117">-LastName</span></span>
<span data-ttu-id="07ada-118">Gibt den letzten Namen des Zertifikat Administrators an.</span><span class="sxs-lookup"><span data-stu-id="07ada-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="07ada-119">-Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="07ada-119">-PhoneNumber</span></span>
<span data-ttu-id="07ada-120">Gibt die Telefonnummer des Zertifikat Administrators an.</span><span class="sxs-lookup"><span data-stu-id="07ada-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="07ada-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="07ada-121">-Confirm</span></span>
<span data-ttu-id="07ada-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="07ada-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07ada-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07ada-123">-WhatIf</span></span>
<span data-ttu-id="07ada-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07ada-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07ada-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07ada-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07ada-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07ada-126">CommonParameters</span></span>
<span data-ttu-id="07ada-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07ada-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07ada-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07ada-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07ada-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07ada-129">INPUTS</span></span>

### <span data-ttu-id="07ada-130">Keine</span><span class="sxs-lookup"><span data-stu-id="07ada-130">None</span></span>
<span data-ttu-id="07ada-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="07ada-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="07ada-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07ada-132">OUTPUTS</span></span>

### <span data-ttu-id="07ada-133">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="07ada-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="07ada-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="07ada-134">NOTES</span></span>

## <span data-ttu-id="07ada-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07ada-135">RELATED LINKS</span></span>

[<span data-ttu-id="07ada-136">Neu – AzKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="07ada-136">New-AzKeyVaultCertificateOrganizationDetails</span></span>](./New-AzKeyVaultCertificateOrganizationDetails.md)

