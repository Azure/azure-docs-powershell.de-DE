---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D08CB0A0-A0A9-4E0A-B1AB-A19A655B501B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5fd66813dcfc08f5e2f5276c4019443f9166945d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005802"
---
# <span data-ttu-id="a24cc-101">Get-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="a24cc-101">Get-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="a24cc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a24cc-102">SYNOPSIS</span></span>
<span data-ttu-id="a24cc-103">Dieses Cmdlet ruft die Remote Desktop Erweiterung des Cloud-Diensts ab, die für alle Rollen oder benannten Rollen in einem bestimmten Bereitstellungs Steckplatz angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="a24cc-103">This cmdlet gets the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="a24cc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a24cc-104">SYNTAX</span></span>

```
Get-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a24cc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a24cc-105">DESCRIPTION</span></span>
<span data-ttu-id="a24cc-106">Das Cmdlet " **Get-AzureServiceRemoteDesktopExtension** " Ruft die Remote Desktop Erweiterung des Cloud-Diensts auf, die für alle Rollen oder benannten Rollen an einem bestimmten Bereitstellungs Steckplatz angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="a24cc-106">The **Get-AzureServiceRemoteDesktopExtension** cmdlet gets the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="a24cc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a24cc-107">EXAMPLES</span></span>

### <span data-ttu-id="a24cc-108">Beispiel 1: Abrufen der Remote Desktop Erweiterung für den angegebenen Dienst</span><span class="sxs-lookup"><span data-stu-id="a24cc-108">Example 1: Get remote desktop extension for the specified service</span></span>
```
PS C:\> Get-AzureServiceRemoteDesktopExtension -ServiceName $svc
```

<span data-ttu-id="a24cc-109">Mit diesem Befehl wird die Remote Desktop Erweiterung für den angegebenen Dienst abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a24cc-109">This command gets the remote desktop extension for the specified service.</span></span>

## <span data-ttu-id="a24cc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a24cc-110">PARAMETERS</span></span>

### <span data-ttu-id="a24cc-111">-Information</span><span class="sxs-lookup"><span data-stu-id="a24cc-111">-InformationAction</span></span>
<span data-ttu-id="a24cc-112">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="a24cc-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a24cc-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a24cc-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a24cc-114">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="a24cc-114">Continue</span></span>
- <span data-ttu-id="a24cc-115">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="a24cc-115">Ignore</span></span>
- <span data-ttu-id="a24cc-116">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="a24cc-116">Inquire</span></span>
- <span data-ttu-id="a24cc-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a24cc-117">SilentlyContinue</span></span>
- <span data-ttu-id="a24cc-118">Beenden</span><span class="sxs-lookup"><span data-stu-id="a24cc-118">Stop</span></span>
- <span data-ttu-id="a24cc-119">Anhalten</span><span class="sxs-lookup"><span data-stu-id="a24cc-119">Suspend</span></span>

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

### <span data-ttu-id="a24cc-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a24cc-120">-InformationVariable</span></span>
<span data-ttu-id="a24cc-121">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="a24cc-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a24cc-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="a24cc-122">-Profile</span></span>
<span data-ttu-id="a24cc-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a24cc-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a24cc-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="a24cc-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a24cc-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a24cc-125">-ServiceName</span></span>
<span data-ttu-id="a24cc-126">Gibt den Azure-Dienstnamen der Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="a24cc-126">Specifies the Azure service name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a24cc-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="a24cc-127">-Slot</span></span>
<span data-ttu-id="a24cc-128">Gibt die Umgebung der Bereitstellung an, die geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a24cc-128">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="a24cc-129">Die akzeptablen Werte für diesen Parameter sind: Production oder Staging.</span><span class="sxs-lookup"><span data-stu-id="a24cc-129">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="a24cc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a24cc-130">CommonParameters</span></span>
<span data-ttu-id="a24cc-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a24cc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a24cc-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a24cc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a24cc-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a24cc-133">INPUTS</span></span>

## <span data-ttu-id="a24cc-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a24cc-134">OUTPUTS</span></span>

## <span data-ttu-id="a24cc-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="a24cc-135">NOTES</span></span>

## <span data-ttu-id="a24cc-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a24cc-136">RELATED LINKS</span></span>

[<span data-ttu-id="a24cc-137">Satz-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="a24cc-137">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


