---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2664607C-FF95-4EB7-869E-A421343B0517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 231f24a20471d8a4639b091c10d0e04f65b71b76
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005805"
---
# <span data-ttu-id="b52fe-101">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="b52fe-101">Get-AzureServiceExtension</span></span>

## <span data-ttu-id="b52fe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b52fe-102">SYNOPSIS</span></span>
<span data-ttu-id="b52fe-103">Ruft Cloud-Diensterweiterungen ab, die auf eine Bereitstellung angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="b52fe-103">Gets cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="b52fe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b52fe-104">SYNTAX</span></span>

```
Get-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-ExtensionName] <String>]
 [[-ProviderNamespace] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b52fe-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b52fe-105">DESCRIPTION</span></span>
<span data-ttu-id="b52fe-106">Das Cmdlet " **Get-AzureServiceExtension** " ruft vorhandene Cloud-Diensterweiterungen ab, die auf eine Bereitstellung angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="b52fe-106">The **Get-AzureServiceExtension** cmdlet gets existing cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="b52fe-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b52fe-107">EXAMPLES</span></span>

### <span data-ttu-id="b52fe-108">Beispiel 1: Abrufen einer angegebenen Erweiterung</span><span class="sxs-lookup"><span data-stu-id="b52fe-108">Example 1: Get a specified extension</span></span>
```
PS C:\> Get-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions"
```

<span data-ttu-id="b52fe-109">Mit diesem Befehl wird die Cloud-Diensterweiterung mit dem angegebenen Namen und Namespace abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b52fe-109">This command gets the cloud service extension with the specified name and namespace.</span></span>

## <span data-ttu-id="b52fe-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b52fe-110">PARAMETERS</span></span>

### <span data-ttu-id="b52fe-111">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="b52fe-111">-ExtensionName</span></span>
<span data-ttu-id="b52fe-112">Gibt den Namen der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="b52fe-112">Specifies the extension name.</span></span>

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

### <span data-ttu-id="b52fe-113">-Information</span><span class="sxs-lookup"><span data-stu-id="b52fe-113">-InformationAction</span></span>
<span data-ttu-id="b52fe-114">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="b52fe-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b52fe-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b52fe-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b52fe-116">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="b52fe-116">Continue</span></span>
- <span data-ttu-id="b52fe-117">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="b52fe-117">Ignore</span></span>
- <span data-ttu-id="b52fe-118">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="b52fe-118">Inquire</span></span>
- <span data-ttu-id="b52fe-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b52fe-119">SilentlyContinue</span></span>
- <span data-ttu-id="b52fe-120">Beenden</span><span class="sxs-lookup"><span data-stu-id="b52fe-120">Stop</span></span>
- <span data-ttu-id="b52fe-121">Anhalten</span><span class="sxs-lookup"><span data-stu-id="b52fe-121">Suspend</span></span>

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

### <span data-ttu-id="b52fe-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b52fe-122">-InformationVariable</span></span>
<span data-ttu-id="b52fe-123">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="b52fe-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b52fe-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="b52fe-124">-Profile</span></span>
<span data-ttu-id="b52fe-125">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="b52fe-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b52fe-126">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b52fe-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b52fe-127">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="b52fe-127">-ProviderNamespace</span></span>
<span data-ttu-id="b52fe-128">Gibt den Namespace des Erweiterungs Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="b52fe-128">Specifies the extension provider namespace.</span></span>

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

### <span data-ttu-id="b52fe-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b52fe-129">-ServiceName</span></span>
<span data-ttu-id="b52fe-130">Gibt den Azure-Dienstnamen der Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="b52fe-130">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="b52fe-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="b52fe-131">-Slot</span></span>
<span data-ttu-id="b52fe-132">Gibt die Bereitstellungsumgebung an.</span><span class="sxs-lookup"><span data-stu-id="b52fe-132">Specifies the deployment environment.</span></span>
<span data-ttu-id="b52fe-133">Die akzeptablen Werte für diesen Parameter sind: Production oder Staging.</span><span class="sxs-lookup"><span data-stu-id="b52fe-133">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="b52fe-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b52fe-134">CommonParameters</span></span>
<span data-ttu-id="b52fe-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b52fe-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b52fe-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b52fe-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b52fe-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b52fe-137">INPUTS</span></span>

## <span data-ttu-id="b52fe-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b52fe-138">OUTPUTS</span></span>

## <span data-ttu-id="b52fe-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="b52fe-139">NOTES</span></span>

## <span data-ttu-id="b52fe-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b52fe-140">RELATED LINKS</span></span>

[<span data-ttu-id="b52fe-141">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="b52fe-141">Remove-AzureServiceExtension</span></span>](./Remove-AzureServiceExtension.md)

[<span data-ttu-id="b52fe-142">Satz-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="b52fe-142">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


