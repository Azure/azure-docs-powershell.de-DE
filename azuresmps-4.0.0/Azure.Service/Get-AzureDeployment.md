---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2171943B-D1AC-45FD-99FD-DD0C14AFC60C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38990d3084cf5f494dc811ec6fe458003b8313c9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006561"
---
# <span data-ttu-id="2c424-101">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="2c424-101">Get-AzureDeployment</span></span>

## <span data-ttu-id="2c424-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2c424-102">SYNOPSIS</span></span>
<span data-ttu-id="2c424-103">Ruft Details einer Bereitstellung ab.</span><span class="sxs-lookup"><span data-stu-id="2c424-103">Gets details of a deployment.</span></span>

## <span data-ttu-id="2c424-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c424-104">SYNTAX</span></span>

```
Get-AzureDeployment [-ServiceName] <String> [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2c424-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c424-105">DESCRIPTION</span></span>
<span data-ttu-id="2c424-106">Das Cmdlet " **Get-AzureDeployment** " ruft Details einer Azure-Bereitstellung ab.</span><span class="sxs-lookup"><span data-stu-id="2c424-106">The **Get-AzureDeployment** cmdlet gets details of an Azure deployment.</span></span>
<span data-ttu-id="2c424-107">Geben Sie den Namen des Azure-Diensts und den Steckplatz der Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="2c424-107">Specify the name of the Azure service and the slot of the deployment.</span></span>

## <span data-ttu-id="2c424-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c424-108">EXAMPLES</span></span>

### <span data-ttu-id="2c424-109">Beispiel 1: Abrufen von Details für eine Produktionsbereitstellung</span><span class="sxs-lookup"><span data-stu-id="2c424-109">Example 1: Get details for a production deployment</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="2c424-110">Dieser Befehl gibt die Details der Bereitstellung für den Dienst mit dem Namen ContosoService zurück.</span><span class="sxs-lookup"><span data-stu-id="2c424-110">This command returns the details of the deployment for the service named ContosoService.</span></span>
<span data-ttu-id="2c424-111">Mit diesem Befehl wird kein Steckplatz angegeben.</span><span class="sxs-lookup"><span data-stu-id="2c424-111">This command does not specify a slot.</span></span>
<span data-ttu-id="2c424-112">Daher verwendet der Befehl den Standardwert von Production.</span><span class="sxs-lookup"><span data-stu-id="2c424-112">Therefore, the command uses the default value of Production.</span></span>

### <span data-ttu-id="2c424-113">Beispiel 2: Abrufen von Details für eine Staging-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="2c424-113">Example 2: Get details for a staging deployment</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Staging"
```

<span data-ttu-id="2c424-114">Dieser Befehl gibt die Details der Staging-Bereitstellung von ContosoService zurück.</span><span class="sxs-lookup"><span data-stu-id="2c424-114">This command returns the details of the staging deployment of ContosoService.</span></span>

## <span data-ttu-id="2c424-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c424-115">PARAMETERS</span></span>

### <span data-ttu-id="2c424-116">-Information</span><span class="sxs-lookup"><span data-stu-id="2c424-116">-InformationAction</span></span>
<span data-ttu-id="2c424-117">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="2c424-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2c424-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2c424-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2c424-119">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="2c424-119">Continue</span></span>
- <span data-ttu-id="2c424-120">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="2c424-120">Ignore</span></span>
- <span data-ttu-id="2c424-121">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="2c424-121">Inquire</span></span>
- <span data-ttu-id="2c424-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2c424-122">SilentlyContinue</span></span>
- <span data-ttu-id="2c424-123">Beenden</span><span class="sxs-lookup"><span data-stu-id="2c424-123">Stop</span></span>
- <span data-ttu-id="2c424-124">Anhalten</span><span class="sxs-lookup"><span data-stu-id="2c424-124">Suspend</span></span>

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

### <span data-ttu-id="2c424-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2c424-125">-InformationVariable</span></span>
<span data-ttu-id="2c424-126">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="2c424-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2c424-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="2c424-127">-Profile</span></span>
<span data-ttu-id="2c424-128">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="2c424-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2c424-129">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="2c424-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2c424-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2c424-130">-ServiceName</span></span>
<span data-ttu-id="2c424-131">Gibt den Namen des Diensts an.</span><span class="sxs-lookup"><span data-stu-id="2c424-131">Specifies the name of the service.</span></span>

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

### <span data-ttu-id="2c424-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="2c424-132">-Slot</span></span>
<span data-ttu-id="2c424-133">Gibt die Umgebung der Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="2c424-133">Specifies the environment of the deployment.</span></span>
<span data-ttu-id="2c424-134">Gültige Werte sind: Staging oder Production.</span><span class="sxs-lookup"><span data-stu-id="2c424-134">Valid values are: Staging or Production.</span></span>
<span data-ttu-id="2c424-135">Der Standardwert ist Production.</span><span class="sxs-lookup"><span data-stu-id="2c424-135">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c424-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c424-136">CommonParameters</span></span>
<span data-ttu-id="2c424-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c424-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c424-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c424-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c424-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2c424-139">INPUTS</span></span>

## <span data-ttu-id="2c424-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2c424-140">OUTPUTS</span></span>

## <span data-ttu-id="2c424-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="2c424-141">NOTES</span></span>

## <span data-ttu-id="2c424-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2c424-142">RELATED LINKS</span></span>

[<span data-ttu-id="2c424-143">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="2c424-143">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="2c424-144">Verschieben-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="2c424-144">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="2c424-145">Neu – AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="2c424-145">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="2c424-146">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="2c424-146">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="2c424-147">Satz-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="2c424-147">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


