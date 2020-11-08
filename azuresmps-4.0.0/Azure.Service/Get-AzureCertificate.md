---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7BEFA810-685C-4553-BED8-4CD6BCF8A5FE
online version: ''
schema: 2.0.0
ms.openlocfilehash: d88784e5d4fdd153700bd3879262198e5dd3807a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006562"
---
# <span data-ttu-id="c3f31-101">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="c3f31-101">Get-AzureCertificate</span></span>

## <span data-ttu-id="c3f31-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3f31-102">SYNOPSIS</span></span>
<span data-ttu-id="c3f31-103">Ruft ein Certificate-Objekt aus einem Azure-Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="c3f31-103">Gets a certificate object from an Azure service.</span></span>

## <span data-ttu-id="c3f31-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3f31-104">SYNTAX</span></span>

```
Get-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm <String>] [-Thumbprint <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="c3f31-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3f31-105">DESCRIPTION</span></span>
<span data-ttu-id="c3f31-106">Das Cmdlet " **Get-AzureCertificate** " Ruft ein Certificate-Objekt aus einem Azure-Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="c3f31-106">The **Get-AzureCertificate** cmdlet gets a certificate object from an Azure service.</span></span>

## <span data-ttu-id="c3f31-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3f31-107">EXAMPLES</span></span>

### <span data-ttu-id="c3f31-108">Beispiel 1: Abrufen von Zertifikaten von einem Dienst</span><span class="sxs-lookup"><span data-stu-id="c3f31-108">Example 1: Get certificates from a service</span></span>
```
PS C:\> $AzureCert = Get-AzureCertificate -ServiceName "ContosoService"
```

<span data-ttu-id="c3f31-109">Dieser Befehl ruft Certificate-Objekte aus dem Dienst mit dem Namen ContosoService ab und speichert Sie dann in der $AzureCert-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c3f31-109">This command gets certificate objects from the service named ContosoService, and then stores them in the $AzureCert variable.</span></span>

### <span data-ttu-id="c3f31-110">Beispiel 2: Abrufen eines Zertifikats von einem Dienst</span><span class="sxs-lookup"><span data-stu-id="c3f31-110">Example 2: Get a certificate from a service</span></span>
```
PS C:\> $AzureCert = Get-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

<span data-ttu-id="c3f31-111">Dieser Befehl ruft das vom angegebenen Fingerabdruck identifizierte Certificate-Objekt aus dem Dienst mit dem Namen ContosoService ab und speichert es dann in der $AzureCert-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c3f31-111">This command gets the certificate object identified by the specified thumbprint from the service named ContosoService, and then stores it in the $AzureCert variable.</span></span>

## <span data-ttu-id="c3f31-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3f31-112">PARAMETERS</span></span>

### <span data-ttu-id="c3f31-113">-Information</span><span class="sxs-lookup"><span data-stu-id="c3f31-113">-InformationAction</span></span>
<span data-ttu-id="c3f31-114">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="c3f31-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c3f31-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3f31-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c3f31-116">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="c3f31-116">Continue</span></span>
- <span data-ttu-id="c3f31-117">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="c3f31-117">Ignore</span></span>
- <span data-ttu-id="c3f31-118">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="c3f31-118">Inquire</span></span>
- <span data-ttu-id="c3f31-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c3f31-119">SilentlyContinue</span></span>
- <span data-ttu-id="c3f31-120">Beenden</span><span class="sxs-lookup"><span data-stu-id="c3f31-120">Stop</span></span>
- <span data-ttu-id="c3f31-121">Anhalten</span><span class="sxs-lookup"><span data-stu-id="c3f31-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3f31-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c3f31-122">-InformationVariable</span></span>
<span data-ttu-id="c3f31-123">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="c3f31-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3f31-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="c3f31-124">-Profile</span></span>
<span data-ttu-id="c3f31-125">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c3f31-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c3f31-126">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c3f31-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c3f31-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c3f31-127">-ServiceName</span></span>
<span data-ttu-id="c3f31-128">Gibt den Namen des Azure-Diensts an, von dem dieses Cmdlet ein Zertifikat erhält.</span><span class="sxs-lookup"><span data-stu-id="c3f31-128">Specifies the name of the Azure service from which this cmdlet gets a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3f31-129">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="c3f31-129">-Thumbprint</span></span>
<span data-ttu-id="c3f31-130">Gibt den Fingerabdruck des Zertifikats an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="c3f31-130">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c3f31-131">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="c3f31-131">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="c3f31-132">Gibt den Algorithmus an, der zum Erstellen des Zertifikat Fingerabdrucks verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3f31-132">Specifies the algorithm that is used to create the certificate thumbprint.</span></span>

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

### <span data-ttu-id="c3f31-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3f31-133">CommonParameters</span></span>
<span data-ttu-id="c3f31-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3f31-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3f31-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3f31-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3f31-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3f31-136">INPUTS</span></span>

## <span data-ttu-id="c3f31-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3f31-137">OUTPUTS</span></span>

### <span data-ttu-id="c3f31-138">Certificatecontext</span><span class="sxs-lookup"><span data-stu-id="c3f31-138">CertificateContext</span></span>

## <span data-ttu-id="c3f31-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3f31-139">NOTES</span></span>

## <span data-ttu-id="c3f31-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3f31-140">RELATED LINKS</span></span>

[<span data-ttu-id="c3f31-141">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="c3f31-141">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="c3f31-142">Neu – AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="c3f31-142">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)

[<span data-ttu-id="c3f31-143">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="c3f31-143">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


