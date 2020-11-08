---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E3D405D-69FB-42C2-8A5B-BDBD27B63088
online version: ''
schema: 2.0.0
ms.openlocfilehash: 503c2e0a076be3f31b6435a30dc658af9b45835a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006373"
---
# <span data-ttu-id="b22f6-101">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="b22f6-101">Remove-AzureCertificate</span></span>

## <span data-ttu-id="b22f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b22f6-102">SYNOPSIS</span></span>
<span data-ttu-id="b22f6-103">Entfernt ein Zertifikat aus einem Azure-Dienst.</span><span class="sxs-lookup"><span data-stu-id="b22f6-103">Removes a certificate from an Azure service.</span></span>

## <span data-ttu-id="b22f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b22f6-104">SYNTAX</span></span>

```
Remove-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b22f6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b22f6-105">DESCRIPTION</span></span>
<span data-ttu-id="b22f6-106">Das Cmdlet **Remove-AzureCertificate** entfernt ein Zertifikat aus einem Azure-Dienst.</span><span class="sxs-lookup"><span data-stu-id="b22f6-106">The **Remove-AzureCertificate** cmdlet removes a certificate from an Azure service.</span></span>

## <span data-ttu-id="b22f6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b22f6-107">EXAMPLES</span></span>

### <span data-ttu-id="b22f6-108">Beispiel 1: Entfernen eines Zertifikats aus einem Dienst</span><span class="sxs-lookup"><span data-stu-id="b22f6-108">Example 1: Remove a certificate from a service</span></span>
```
PS C:\> Remove-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

<span data-ttu-id="b22f6-109">Dieser Befehl entfernt das Certificate-Objekt, das den angegebenen Fingerabdruck hat, aus dem clouddienst.</span><span class="sxs-lookup"><span data-stu-id="b22f6-109">This command removes the certificate object that has the specified thumbprint from the cloud service.</span></span>

### <span data-ttu-id="b22f6-110">Beispiel 2: Entfernen aller Zertifikate aus einem Dienst</span><span class="sxs-lookup"><span data-stu-id="b22f6-110">Example 2: Remove all certificates from a service</span></span>
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" | Remove-AzureCertificate
```

<span data-ttu-id="b22f6-111">Dieser Befehl ruft alle Zertifikate des Diensts mit dem Namen ContosoService mit dem Cmdlet **Get-AzureCertificate** ab.</span><span class="sxs-lookup"><span data-stu-id="b22f6-111">This command gets all the certificates from the service named ContosoService by using the **Get-AzureCertificate** cmdlet.</span></span>
<span data-ttu-id="b22f6-112">Der Befehl übergibt jedes Zertifikat mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b22f6-112">The command passes each certificate to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b22f6-113">Dieses Cmdlet entfernt jedes Zertifikat aus dem clouddienst.</span><span class="sxs-lookup"><span data-stu-id="b22f6-113">That cmdlet removes each certificate from the cloud service.</span></span>

### <span data-ttu-id="b22f6-114">Beispiel 3: Entfernen aller Zertifikate aus einem Dienst, die einen bestimmten Fingerabdruckalgorithmus verwenden</span><span class="sxs-lookup"><span data-stu-id="b22f6-114">Example 3: Remove all certificates from a service that use a specific thumbprint algorithm</span></span>
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" -ThumbprintAlgorithm "sha1" | Remove-AzureCertificate
```

<span data-ttu-id="b22f6-115">Dieser Befehl ruft alle Zertifikate des Diensts mit dem Namen ContosoService ab, die den SHA1-Fingerabdruckalgorithmus verwenden.</span><span class="sxs-lookup"><span data-stu-id="b22f6-115">This command gets all the certificates from the service named ContosoService that use the sha1 thumbprint algorithm.</span></span>
<span data-ttu-id="b22f6-116">Der Befehl übergibt jedes Zertifikat an das aktuelle Cmdlet, wodurch jedes Zertifikat entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b22f6-116">The command passes each certificate to the current cmdlet, which removes each certificate.</span></span>

## <span data-ttu-id="b22f6-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="b22f6-117">PARAMETERS</span></span>

### <span data-ttu-id="b22f6-118">-Information</span><span class="sxs-lookup"><span data-stu-id="b22f6-118">-InformationAction</span></span>
<span data-ttu-id="b22f6-119">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="b22f6-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b22f6-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b22f6-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b22f6-121">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="b22f6-121">Continue</span></span>
- <span data-ttu-id="b22f6-122">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="b22f6-122">Ignore</span></span>
- <span data-ttu-id="b22f6-123">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="b22f6-123">Inquire</span></span>
- <span data-ttu-id="b22f6-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b22f6-124">SilentlyContinue</span></span>
- <span data-ttu-id="b22f6-125">Beenden</span><span class="sxs-lookup"><span data-stu-id="b22f6-125">Stop</span></span>
- <span data-ttu-id="b22f6-126">Anhalten</span><span class="sxs-lookup"><span data-stu-id="b22f6-126">Suspend</span></span>

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

### <span data-ttu-id="b22f6-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b22f6-127">-InformationVariable</span></span>
<span data-ttu-id="b22f6-128">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="b22f6-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b22f6-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="b22f6-129">-Profile</span></span>
<span data-ttu-id="b22f6-130">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="b22f6-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b22f6-131">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b22f6-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b22f6-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b22f6-132">-ServiceName</span></span>
<span data-ttu-id="b22f6-133">Gibt den Namen des Azure-Diensts an, aus dem dieses Cmdlet ein Zertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="b22f6-133">Specifies the name of the Azure service from which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="b22f6-134">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="b22f6-134">-Thumbprint</span></span>
<span data-ttu-id="b22f6-135">Gibt den Fingerabdruck des Zertifikats an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b22f6-135">Specifies the thumbprint of the certificate that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b22f6-136">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="b22f6-136">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="b22f6-137">Gibt den Algorithmus an, der zum Erstellen des Zertifikat Fingerabdrucks verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b22f6-137">Specifies the algorithm that is used to create the certificate thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b22f6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b22f6-138">CommonParameters</span></span>
<span data-ttu-id="b22f6-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b22f6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b22f6-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b22f6-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b22f6-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b22f6-141">INPUTS</span></span>

## <span data-ttu-id="b22f6-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b22f6-142">OUTPUTS</span></span>

### <span data-ttu-id="b22f6-143">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="b22f6-143">ManagementOperationContext</span></span>

## <span data-ttu-id="b22f6-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="b22f6-144">NOTES</span></span>

## <span data-ttu-id="b22f6-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b22f6-145">RELATED LINKS</span></span>

[<span data-ttu-id="b22f6-146">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="b22f6-146">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="b22f6-147">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="b22f6-147">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="b22f6-148">Neu – AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="b22f6-148">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)


