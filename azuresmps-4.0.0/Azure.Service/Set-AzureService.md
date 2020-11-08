---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4A920D84-0005-45A2-8229-FD9436A2CA6D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 927520466299776326229976b355444f9db6c23e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006255"
---
# <span data-ttu-id="a062b-101">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="a062b-101">Set-AzureService</span></span>

## <span data-ttu-id="a062b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a062b-102">SYNOPSIS</span></span>
<span data-ttu-id="a062b-103">Legt die Bezeichnung und Beschreibung des angegebenen Microsoft Azure-Diensts fest oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="a062b-103">Sets or updates the label and description of the specified Microsoft Azure service.</span></span>

## <span data-ttu-id="a062b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a062b-104">SYNTAX</span></span>

```
Set-AzureService [-ServiceName] <String> [[-Label] <String>] [[-Description] <String>]
 [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a062b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a062b-105">DESCRIPTION</span></span>
<span data-ttu-id="a062b-106">Das Cmdlet " **Satz-AzureService** " weist einem Dienst im aktuellen Abonnement eine Bezeichnung und eine Beschreibung zu.</span><span class="sxs-lookup"><span data-stu-id="a062b-106">The **Set-AzureService** cmdlet assigns a label and description to a service in the current subscription.</span></span>

## <span data-ttu-id="a062b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a062b-107">EXAMPLES</span></span>

### <span data-ttu-id="a062b-108">Beispiel 1: Aktualisieren der Bezeichnung und Beschreibung für einen Dienst</span><span class="sxs-lookup"><span data-stu-id="a062b-108">Example 1: Update the label and description for a service</span></span>
```
PS C:\> C:\PS>Set-AzureService -ServiceName "MySvc1" -Label "MyTestSvc1" -Description "My service for testing out new configurations"
```

<span data-ttu-id="a062b-109">Mit diesem Befehl wird die Bezeichnung auf "MyTestSvc1" und die Beschreibung für den MyTestSvc1-Dienst "Mein Dienst zum Testen neuer Konfigurationen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a062b-109">This command sets the label to "MyTestSvc1" and the description to "My service for testing out new configurations" for the MyTestSvc1 service.</span></span>

## <span data-ttu-id="a062b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a062b-110">PARAMETERS</span></span>

### <span data-ttu-id="a062b-111">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a062b-111">-Description</span></span>
<span data-ttu-id="a062b-112">Gibt eine Beschreibung für den Azure-Dienst an.</span><span class="sxs-lookup"><span data-stu-id="a062b-112">Specifies a description for the Azure service.</span></span>
<span data-ttu-id="a062b-113">Die Beschreibung kann bis zu 1024 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="a062b-113">The description may be up to 1024 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a062b-114">-Information</span><span class="sxs-lookup"><span data-stu-id="a062b-114">-InformationAction</span></span>
<span data-ttu-id="a062b-115">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="a062b-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a062b-116">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a062b-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a062b-117">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="a062b-117">Continue</span></span>
- <span data-ttu-id="a062b-118">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="a062b-118">Ignore</span></span>
- <span data-ttu-id="a062b-119">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="a062b-119">Inquire</span></span>
- <span data-ttu-id="a062b-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a062b-120">SilentlyContinue</span></span>
- <span data-ttu-id="a062b-121">Beenden</span><span class="sxs-lookup"><span data-stu-id="a062b-121">Stop</span></span>
- <span data-ttu-id="a062b-122">Anhalten</span><span class="sxs-lookup"><span data-stu-id="a062b-122">Suspend</span></span>

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

### <span data-ttu-id="a062b-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a062b-123">-InformationVariable</span></span>
<span data-ttu-id="a062b-124">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="a062b-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a062b-125">-Label</span><span class="sxs-lookup"><span data-stu-id="a062b-125">-Label</span></span>
<span data-ttu-id="a062b-126">Gibt eine Bezeichnung für den Azure-Dienst an.</span><span class="sxs-lookup"><span data-stu-id="a062b-126">Specifies a label for the Azure service.</span></span>
<span data-ttu-id="a062b-127">Die Beschriftung kann bis zu 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="a062b-127">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a062b-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="a062b-128">-Profile</span></span>
<span data-ttu-id="a062b-129">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a062b-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a062b-130">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="a062b-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a062b-131">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="a062b-131">-ReverseDnsFqdn</span></span>
<span data-ttu-id="a062b-132">Gibt den vollqualifizierten Domänennamen für Reverse-DNS an.</span><span class="sxs-lookup"><span data-stu-id="a062b-132">Specifies the fully qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a062b-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a062b-133">-ServiceName</span></span>
<span data-ttu-id="a062b-134">Gibt den Namen des Azure-Diensts an, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a062b-134">Specifies the name of the Azure service to update.</span></span>

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

### <span data-ttu-id="a062b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a062b-135">CommonParameters</span></span>
<span data-ttu-id="a062b-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a062b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a062b-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a062b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a062b-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a062b-138">INPUTS</span></span>

## <span data-ttu-id="a062b-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a062b-139">OUTPUTS</span></span>

### <span data-ttu-id="a062b-140">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="a062b-140">ManagementOperationContext</span></span>

## <span data-ttu-id="a062b-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="a062b-141">NOTES</span></span>

## <span data-ttu-id="a062b-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a062b-142">RELATED LINKS</span></span>

[<span data-ttu-id="a062b-143">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="a062b-143">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="a062b-144">Neu – AzureService</span><span class="sxs-lookup"><span data-stu-id="a062b-144">New-AzureService</span></span>](./New-AzureService.md)


