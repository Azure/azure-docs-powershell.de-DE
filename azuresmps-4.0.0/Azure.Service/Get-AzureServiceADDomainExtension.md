---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CF429CF0-2AB2-4E31-8A0D-AE5C8D77A76B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0d1ad08d88cb5b89b0537b19f8ea4aaef0000cbb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005813"
---
# <span data-ttu-id="0f579-101">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="0f579-101">Get-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="0f579-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0f579-102">SYNOPSIS</span></span>
<span data-ttu-id="0f579-103">Ruft die Active Directory-Domänenerweiterung des Cloud-Diensts ab, die für alle Rollen oder benannten Rollen in einem angegebenen Bereitstellungs Steckplatz gilt.</span><span class="sxs-lookup"><span data-stu-id="0f579-103">Gets the cloud service Active Directory (AD) domain extension that applies to all roles or to named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="0f579-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f579-104">SYNTAX</span></span>

```
Get-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0f579-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f579-105">DESCRIPTION</span></span>
<span data-ttu-id="0f579-106">Das Cmdlet " **Get-AzureServiceADDomainExtension** " Ruft die AD-Domänenerweiterung des Cloud-Diensts ab, die für alle Rollen oder benannten Rollen in einem angegebenen Bereitstellungs Steckplatz gilt.</span><span class="sxs-lookup"><span data-stu-id="0f579-106">The **Get-AzureServiceADDomainExtension** cmdlet gets the cloud service AD domain extension that applies to all roles or named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="0f579-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f579-107">EXAMPLES</span></span>

### <span data-ttu-id="0f579-108">Beispiel 1: Abrufen der AD-Domänenerweiterung für einen angegebenen Dienst</span><span class="sxs-lookup"><span data-stu-id="0f579-108">Example 1: Get the AD domain extension for a specified service</span></span>
```
PS C:\> Get-AzureServiceADDomainExtension -ServiceName $Svc
```

<span data-ttu-id="0f579-109">Mit diesem Befehl wird die AD-Domänenerweiterung für den in $SVC angegebenen Dienst abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0f579-109">This command gets the AD domain extension for the service specified in $Svc.</span></span>

## <span data-ttu-id="0f579-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f579-110">PARAMETERS</span></span>

### <span data-ttu-id="0f579-111">-Information</span><span class="sxs-lookup"><span data-stu-id="0f579-111">-InformationAction</span></span>
<span data-ttu-id="0f579-112">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="0f579-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0f579-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0f579-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0f579-114">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="0f579-114">Continue</span></span>
- <span data-ttu-id="0f579-115">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="0f579-115">Ignore</span></span>
- <span data-ttu-id="0f579-116">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="0f579-116">Inquire</span></span>
- <span data-ttu-id="0f579-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0f579-117">SilentlyContinue</span></span>
- <span data-ttu-id="0f579-118">Beenden</span><span class="sxs-lookup"><span data-stu-id="0f579-118">Stop</span></span>
- <span data-ttu-id="0f579-119">Anhalten</span><span class="sxs-lookup"><span data-stu-id="0f579-119">Suspend</span></span>

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

### <span data-ttu-id="0f579-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0f579-120">-InformationVariable</span></span>
<span data-ttu-id="0f579-121">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="0f579-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0f579-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="0f579-122">-Profile</span></span>
<span data-ttu-id="0f579-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="0f579-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0f579-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="0f579-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0f579-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0f579-125">-ServiceName</span></span>
<span data-ttu-id="0f579-126">Gibt den Azure-Dienstnamen der Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="0f579-126">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="0f579-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="0f579-127">-Slot</span></span>
<span data-ttu-id="0f579-128">Gibt die Bereitstellungsumgebung an.</span><span class="sxs-lookup"><span data-stu-id="0f579-128">Specifies the deployment environment.</span></span>
<span data-ttu-id="0f579-129">Die akzeptablen Werte für diesen Parameter sind: Production oder Staging.</span><span class="sxs-lookup"><span data-stu-id="0f579-129">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="0f579-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f579-130">CommonParameters</span></span>
<span data-ttu-id="0f579-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f579-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f579-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f579-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f579-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0f579-133">INPUTS</span></span>

## <span data-ttu-id="0f579-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0f579-134">OUTPUTS</span></span>

## <span data-ttu-id="0f579-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="0f579-135">NOTES</span></span>

## <span data-ttu-id="0f579-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0f579-136">RELATED LINKS</span></span>

[<span data-ttu-id="0f579-137">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="0f579-137">Remove-AzureServiceADDomainExtension</span></span>](./Remove-AzureServiceADDomainExtension.md)

[<span data-ttu-id="0f579-138">Satz-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="0f579-138">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


