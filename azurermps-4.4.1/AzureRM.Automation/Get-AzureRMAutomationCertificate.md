---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
ms.openlocfilehash: 956569d407918d0891af6aa1d6f8f09eb61b9a98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664483"
---
# <span data-ttu-id="cfe92-101">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="cfe92-101">Get-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="cfe92-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cfe92-102">SYNOPSIS</span></span>
<span data-ttu-id="cfe92-103">Ruft Automatisierungs Zertifikate ab.</span><span class="sxs-lookup"><span data-stu-id="cfe92-103">Gets Automation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfe92-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfe92-104">SYNTAX</span></span>

### <span data-ttu-id="cfe92-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="cfe92-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfe92-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="cfe92-106">ByCertificateName</span></span>
```
Get-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfe92-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cfe92-107">DESCRIPTION</span></span>
<span data-ttu-id="cfe92-108">Das Cmdlet " **Get-AzureRmAutomationCertificate** " ruft mindestens ein Azure-Automatisierungs Zertifikat ab.</span><span class="sxs-lookup"><span data-stu-id="cfe92-108">The **Get-AzureRmAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="cfe92-109">Standardmäßig werden mit diesem Cmdlet alle Zertifikate abgerufen.</span><span class="sxs-lookup"><span data-stu-id="cfe92-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="cfe92-110">Geben Sie den Namen eines Zertifikats an, um ein bestimmtes Zertifikat zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cfe92-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="cfe92-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cfe92-111">EXAMPLES</span></span>

### <span data-ttu-id="cfe92-112">Beispiel 1: Abrufen aller Zertifikate</span><span class="sxs-lookup"><span data-stu-id="cfe92-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="cfe92-113">Dieser Befehl ruft Metadaten für alle Zertifikate im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="cfe92-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="cfe92-114">Beispiel 2: Abrufen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="cfe92-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="cfe92-115">Dieser Befehl ruft Metadaten für das Zertifikat mit dem Namen ContosoCertificate ab.</span><span class="sxs-lookup"><span data-stu-id="cfe92-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="cfe92-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfe92-116">PARAMETERS</span></span>

### <span data-ttu-id="cfe92-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cfe92-117">-AutomationAccountName</span></span>
<span data-ttu-id="cfe92-118">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet ein Zertifikat abruft.</span><span class="sxs-lookup"><span data-stu-id="cfe92-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfe92-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cfe92-119">-Name</span></span>
<span data-ttu-id="cfe92-120">Gibt den Namen eines Zertifikats an, das abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="cfe92-120">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfe92-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfe92-121">-ResourceGroupName</span></span>
<span data-ttu-id="cfe92-122">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet ein Automatisierungs Zertifikat erhält.</span><span class="sxs-lookup"><span data-stu-id="cfe92-122">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfe92-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfe92-123">-DefaultProfile</span></span>
<span data-ttu-id="cfe92-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cfe92-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfe92-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfe92-125">CommonParameters</span></span>
<span data-ttu-id="cfe92-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfe92-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfe92-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfe92-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfe92-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cfe92-128">INPUTS</span></span>

## <span data-ttu-id="cfe92-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cfe92-129">OUTPUTS</span></span>

### <span data-ttu-id="cfe92-130">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="cfe92-130">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="cfe92-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="cfe92-131">NOTES</span></span>

## <span data-ttu-id="cfe92-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cfe92-132">RELATED LINKS</span></span>

[<span data-ttu-id="cfe92-133">Neu – AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="cfe92-133">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="cfe92-134">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="cfe92-134">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="cfe92-135">Satz-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="cfe92-135">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


