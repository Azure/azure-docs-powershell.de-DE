---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateadministratordetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
ms.openlocfilehash: 39deb08468912bf727198ec4f90f5f4f0680941f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010191"
---
# <span data-ttu-id="afca7-101">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="afca7-101">New-AzKeyVaultCertificateAdministratorDetail</span></span>

## <span data-ttu-id="afca7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="afca7-102">SYNOPSIS</span></span>
<span data-ttu-id="afca7-103">Erstellt ein Zertifikat Administrator Details-Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="afca7-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="afca7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="afca7-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afca7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="afca7-105">DESCRIPTION</span></span>
<span data-ttu-id="afca7-106">Mit dem Cmdlet **New-AzKeyVaultCertificateAdministratorDetail** wird ein speicherresidentes Zertifikat-Administrator Details-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="afca7-106">The **New-AzKeyVaultCertificateAdministratorDetail** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="afca7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="afca7-107">EXAMPLES</span></span>

### <span data-ttu-id="afca7-108">Beispiel 1: Erstellen eines Zertifikats Administrator Details-Objekts</span><span class="sxs-lookup"><span data-stu-id="afca7-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="afca7-109">Mit diesem Befehl wird ein in-Memory-Zertifikat Administrator Details-Objekt erstellt und dann in der $AdminDetails-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="afca7-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="afca7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="afca7-110">PARAMETERS</span></span>

### <span data-ttu-id="afca7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afca7-111">-DefaultProfile</span></span>
<span data-ttu-id="afca7-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="afca7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="afca7-113">-Email-Email</span><span class="sxs-lookup"><span data-stu-id="afca7-113">-EmailAddress</span></span>
<span data-ttu-id="afca7-114">Gibt die e-Mail-Adresse des Zertifikat Administrators an.</span><span class="sxs-lookup"><span data-stu-id="afca7-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="afca7-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="afca7-115">-FirstName</span></span>
<span data-ttu-id="afca7-116">Gibt den Vornamen des Zertifikat Administrators an.</span><span class="sxs-lookup"><span data-stu-id="afca7-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="afca7-117">-Nachname</span><span class="sxs-lookup"><span data-stu-id="afca7-117">-LastName</span></span>
<span data-ttu-id="afca7-118">Gibt den letzten Namen des Zertifikat Administrators an.</span><span class="sxs-lookup"><span data-stu-id="afca7-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="afca7-119">-Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="afca7-119">-PhoneNumber</span></span>
<span data-ttu-id="afca7-120">Gibt die Telefonnummer des Zertifikat Administrators an.</span><span class="sxs-lookup"><span data-stu-id="afca7-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="afca7-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="afca7-121">-Confirm</span></span>
<span data-ttu-id="afca7-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="afca7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afca7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afca7-123">-WhatIf</span></span>
<span data-ttu-id="afca7-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="afca7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afca7-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="afca7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afca7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afca7-126">CommonParameters</span></span>
<span data-ttu-id="afca7-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afca7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afca7-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="afca7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afca7-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="afca7-129">INPUTS</span></span>

### <span data-ttu-id="afca7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="afca7-130">System.String</span></span>

## <span data-ttu-id="afca7-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="afca7-131">OUTPUTS</span></span>

### <span data-ttu-id="afca7-132">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="afca7-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="afca7-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="afca7-133">NOTES</span></span>

## <span data-ttu-id="afca7-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="afca7-134">RELATED LINKS</span></span>

[<span data-ttu-id="afca7-135">Neu – AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="afca7-135">New-AzKeyVaultCertificateOrganizationDetail</span></span>](./New-AzKeyVaultCertificateOrganizationDetail.md)

