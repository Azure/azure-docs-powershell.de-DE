---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FED10AA9-DD3A-4034-B78E-F9E55290B353
online version: ''
schema: 2.0.0
ms.openlocfilehash: 272969751988d3747788c2a214e8eb7ed509f232
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005869"
---
# <span data-ttu-id="bdce8-101">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bdce8-101">Get-AzureAutomationCertificate</span></span>

## <span data-ttu-id="bdce8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bdce8-102">SYNOPSIS</span></span>

<span data-ttu-id="bdce8-103">Ruft ein Azure-Automatisierungs Zertifikat ab.</span><span class="sxs-lookup"><span data-stu-id="bdce8-103">Gets an Azure Automation certificate.</span></span>

## <span data-ttu-id="bdce8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdce8-104">SYNTAX</span></span>

### <span data-ttu-id="bdce8-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="bdce8-105">ByAll (Default)</span></span>
```
Get-AzureAutomationCertificate -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bdce8-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="bdce8-106">ByCertificateName</span></span>
```
Get-AzureAutomationCertificate -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="bdce8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bdce8-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="bdce8-108">Das Cmdlet " **Get-AzureAutomationCertificate** " ruft mindestens ein Microsoft Azure-Automatisierungs Zertifikat ab.</span><span class="sxs-lookup"><span data-stu-id="bdce8-108">The **Get-AzureAutomationCertificate** cmdlet gets one or more Microsoft Azure Automation certificates.</span></span>
<span data-ttu-id="bdce8-109">Standardmäßig werden alle Zertifikate zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bdce8-109">By default, all certificates are returned.</span></span>
<span data-ttu-id="bdce8-110">Um ein bestimmtes Zertifikat abzurufen, geben Sie dessen Namen an.</span><span class="sxs-lookup"><span data-stu-id="bdce8-110">To get a specific certificate, specify its name.</span></span>

## <span data-ttu-id="bdce8-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bdce8-111">EXAMPLES</span></span>

### <span data-ttu-id="bdce8-112">Beispiel 1: Abrufen aller Zertifikate</span><span class="sxs-lookup"><span data-stu-id="bdce8-112">Example 1: Get all certificates</span></span>
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17"
```

<span data-ttu-id="bdce8-113">Dieser Befehl ruft alle Zertifikate im Azure Automation-Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="bdce8-113">This command gets all certificates in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="bdce8-114">Beispiel 2: Abrufen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="bdce8-114">Example 2: Get a certificate</span></span>
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyUserCertificate"
```

<span data-ttu-id="bdce8-115">Dieser Befehl ruft das Zertifikat mit dem Namen MyUserCertificate ab.</span><span class="sxs-lookup"><span data-stu-id="bdce8-115">This command gets the certificate named MyUserCertificate.</span></span>

## <span data-ttu-id="bdce8-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdce8-116">PARAMETERS</span></span>

### <span data-ttu-id="bdce8-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bdce8-117">-AutomationAccountName</span></span>
<span data-ttu-id="bdce8-118">Gibt den Namen des Automatisierungs Kontos mit dem Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="bdce8-118">Specifies the name of the automation account with the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdce8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bdce8-119">-Name</span></span>
<span data-ttu-id="bdce8-120">Gibt den Namen eines Zertifikats an, das abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="bdce8-120">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdce8-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="bdce8-121">-Profile</span></span>
<span data-ttu-id="bdce8-122">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="bdce8-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bdce8-123">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="bdce8-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdce8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdce8-124">CommonParameters</span></span>
<span data-ttu-id="bdce8-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdce8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdce8-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdce8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdce8-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bdce8-127">INPUTS</span></span>

## <span data-ttu-id="bdce8-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bdce8-128">OUTPUTS</span></span>

### <span data-ttu-id="bdce8-129">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="bdce8-129">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="bdce8-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="bdce8-130">NOTES</span></span>

## <span data-ttu-id="bdce8-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bdce8-131">RELATED LINKS</span></span>

[<span data-ttu-id="bdce8-132">Neu – AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bdce8-132">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="bdce8-133">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bdce8-133">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)

[<span data-ttu-id="bdce8-134">Satz-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bdce8-134">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


