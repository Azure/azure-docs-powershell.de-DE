---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 235DD5D7-BE24-4FBE-88E2-40D1943ED155
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4fb3f35bc64a1431550d4da5aa669e934cd3a7f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005809"
---
# <span data-ttu-id="25f4b-101">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="25f4b-101">Get-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="25f4b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25f4b-102">SYNOPSIS</span></span>
<span data-ttu-id="25f4b-103">Ruft die Erweiterung für die Cloud-Dienst Diagnose ab, die für alle Rollen oder benannten Rollen in einem bestimmten Bereitstellungs Steckplatz angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="25f4b-103">Gets the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="25f4b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25f4b-104">SYNTAX</span></span>

```
Get-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="25f4b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25f4b-105">DESCRIPTION</span></span>
<span data-ttu-id="25f4b-106">Das Cmdlet " **Get-AzureServiceDiagnosticsExtension** " Ruft die Erweiterung für die Cloud-Dienst Diagnose ab, die für alle Rollen oder benannten Rollen in einem bestimmten Bereitstellungs Steckplatz angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="25f4b-106">The **Get-AzureServiceDiagnosticsExtension** cmdlet gets the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="25f4b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25f4b-107">EXAMPLES</span></span>

### <span data-ttu-id="25f4b-108">Beispiel 1: Abrufen der Dienst Diagnose Erweiterung</span><span class="sxs-lookup"><span data-stu-id="25f4b-108">Example 1: Get service diagnostics extension</span></span> 
```
PS C:\> Get-AzureServiceDiagnosticsExtension -ServiceName $Svc
```

<span data-ttu-id="25f4b-109">Dieser Befehl ruft die Dienst Diagnose für einen Dienst über alle Rollen ab.</span><span class="sxs-lookup"><span data-stu-id="25f4b-109">This command gets the service diagnostics for a service, across all roles.</span></span>

## <span data-ttu-id="25f4b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="25f4b-110">PARAMETERS</span></span>

### <span data-ttu-id="25f4b-111">-Information</span><span class="sxs-lookup"><span data-stu-id="25f4b-111">-InformationAction</span></span>
<span data-ttu-id="25f4b-112">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="25f4b-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="25f4b-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="25f4b-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="25f4b-114">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="25f4b-114">Continue</span></span>
- <span data-ttu-id="25f4b-115">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="25f4b-115">Ignore</span></span>
- <span data-ttu-id="25f4b-116">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="25f4b-116">Inquire</span></span>
- <span data-ttu-id="25f4b-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="25f4b-117">SilentlyContinue</span></span>
- <span data-ttu-id="25f4b-118">Beenden</span><span class="sxs-lookup"><span data-stu-id="25f4b-118">Stop</span></span>
- <span data-ttu-id="25f4b-119">Anhalten</span><span class="sxs-lookup"><span data-stu-id="25f4b-119">Suspend</span></span>

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

### <span data-ttu-id="25f4b-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="25f4b-120">-InformationVariable</span></span>
<span data-ttu-id="25f4b-121">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="25f4b-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="25f4b-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="25f4b-122">-Profile</span></span>
<span data-ttu-id="25f4b-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="25f4b-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="25f4b-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="25f4b-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="25f4b-125">-Role</span><span class="sxs-lookup"><span data-stu-id="25f4b-125">-Role</span></span>
<span data-ttu-id="25f4b-126">Gibt ein Array von Rollen an.</span><span class="sxs-lookup"><span data-stu-id="25f4b-126">Specifies an array of roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25f4b-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="25f4b-127">-ServiceName</span></span>
<span data-ttu-id="25f4b-128">Gibt den Azure-Dienstnamen der Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="25f4b-128">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="25f4b-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="25f4b-129">-Slot</span></span>
<span data-ttu-id="25f4b-130">Gibt die Umgebung der Bereitstellung an, die geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="25f4b-130">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="25f4b-131">Die akzeptablen Werte für diesen Parameter sind: Production oder Staging.</span><span class="sxs-lookup"><span data-stu-id="25f4b-131">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="25f4b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25f4b-132">CommonParameters</span></span>
<span data-ttu-id="25f4b-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25f4b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25f4b-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25f4b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25f4b-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25f4b-135">INPUTS</span></span>

## <span data-ttu-id="25f4b-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25f4b-136">OUTPUTS</span></span>

## <span data-ttu-id="25f4b-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="25f4b-137">NOTES</span></span>

## <span data-ttu-id="25f4b-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25f4b-138">RELATED LINKS</span></span>

[<span data-ttu-id="25f4b-139">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="25f4b-139">Remove-AzureServiceDiagnosticsExtension</span></span>](./Remove-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="25f4b-140">Satz-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="25f4b-140">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


