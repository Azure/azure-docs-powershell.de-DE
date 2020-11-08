---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B935B615-1200-4A83-95AF-4F17785793B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a331f3e0ff2797b84c241e64872e3af0841cb106
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006450"
---
# <span data-ttu-id="0b30e-101">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="0b30e-101">Move-AzureDeployment</span></span>

## <span data-ttu-id="0b30e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b30e-102">SYNOPSIS</span></span>
<span data-ttu-id="0b30e-103">Tauscht Bereitstellungen zwischen Produktion und Staging aus.</span><span class="sxs-lookup"><span data-stu-id="0b30e-103">Swaps deployments between production and staging.</span></span>

## <span data-ttu-id="0b30e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b30e-104">SYNTAX</span></span>

```
Move-AzureDeployment [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0b30e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b30e-105">DESCRIPTION</span></span>
<span data-ttu-id="0b30e-106">Das Cmdlet **Move-AzureDeployment** tauscht die virtuellen IP-Adressen von Bereitstellungen in Produktions-und Staging-Umgebungen aus.</span><span class="sxs-lookup"><span data-stu-id="0b30e-106">The **Move-AzureDeployment** cmdlet swaps the virtual IP addresses of deployments in production and staging environments.</span></span>
<span data-ttu-id="0b30e-107">Mit diesem Cmdlet wird eine Bereitstellung, die derzeit in der Stagingumgebung ausgeführt wird, in die Produktionsumgebung und eine Bereitstellung, die in der Produktionsumgebung ausgeführt wird, in der Stagingumgebung ausgetauscht.</span><span class="sxs-lookup"><span data-stu-id="0b30e-107">This cmdlet swaps a deployment that currently runs in the staging environment to the production environment, and a deployment that runs in the production environment to the staging environment.</span></span>
<span data-ttu-id="0b30e-108">Wenn in der Stagingumgebung eine Bereitstellung vorhanden ist und keine Bereitstellung in der Produktionsumgebung erfolgt, verschiebt das Cmdlet die Bereitstellung in die Produktionsumgebung.</span><span class="sxs-lookup"><span data-stu-id="0b30e-108">If there is a deployment in the staging environment and no deployment in the production environment, the cmdlet moves the deployment to production.</span></span>
<span data-ttu-id="0b30e-109">Wenn eine Bereitstellung in der Produktionsumgebung und keine Bereitstellung in der Stagingumgebung vorhanden ist, schlägt das Cmdlet fehl.</span><span class="sxs-lookup"><span data-stu-id="0b30e-109">If there is a deployment in the production environment and no deployment in the staging environment, the cmdlet fails.</span></span>

## <span data-ttu-id="0b30e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b30e-110">EXAMPLES</span></span>

### <span data-ttu-id="0b30e-111">Beispiel 1: Austauschen von Bereitstellungen für einen Dienst</span><span class="sxs-lookup"><span data-stu-id="0b30e-111">Example 1: Swap deployments for a service</span></span>
```
PS C:\> Move-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="0b30e-112">Dieser Befehl tauscht die Bereitstellungen des Diensts mit dem Namen ContosoService zwischen den Produktions-und Staging-Umgebungen aus.</span><span class="sxs-lookup"><span data-stu-id="0b30e-112">This command swaps the deployments of the service named ContosoService between the production and staging environments.</span></span>

## <span data-ttu-id="0b30e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b30e-113">PARAMETERS</span></span>

### <span data-ttu-id="0b30e-114">-Information</span><span class="sxs-lookup"><span data-stu-id="0b30e-114">-InformationAction</span></span>
<span data-ttu-id="0b30e-115">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="0b30e-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0b30e-116">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0b30e-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b30e-117">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="0b30e-117">Continue</span></span>
- <span data-ttu-id="0b30e-118">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="0b30e-118">Ignore</span></span>
- <span data-ttu-id="0b30e-119">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="0b30e-119">Inquire</span></span>
- <span data-ttu-id="0b30e-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0b30e-120">SilentlyContinue</span></span>
- <span data-ttu-id="0b30e-121">Beenden</span><span class="sxs-lookup"><span data-stu-id="0b30e-121">Stop</span></span>
- <span data-ttu-id="0b30e-122">Anhalten</span><span class="sxs-lookup"><span data-stu-id="0b30e-122">Suspend</span></span>

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

### <span data-ttu-id="0b30e-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0b30e-123">-InformationVariable</span></span>
<span data-ttu-id="0b30e-124">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="0b30e-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0b30e-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="0b30e-125">-Profile</span></span>
<span data-ttu-id="0b30e-126">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="0b30e-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0b30e-127">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="0b30e-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0b30e-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0b30e-128">-ServiceName</span></span>
<span data-ttu-id="0b30e-129">Gibt den Namen des Diensts an, für den das Cmdlet Produktions-und Staging-Bereitstellungen vertauscht.</span><span class="sxs-lookup"><span data-stu-id="0b30e-129">Specifies the name of the service for which this cmdlet swaps production and staging deployments.</span></span>

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

### <span data-ttu-id="0b30e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b30e-130">CommonParameters</span></span>
<span data-ttu-id="0b30e-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b30e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b30e-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b30e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b30e-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b30e-133">INPUTS</span></span>

## <span data-ttu-id="0b30e-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b30e-134">OUTPUTS</span></span>

### <span data-ttu-id="0b30e-135">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="0b30e-135">ManagementOperationContext</span></span>

## <span data-ttu-id="0b30e-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b30e-136">NOTES</span></span>

## <span data-ttu-id="0b30e-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b30e-137">RELATED LINKS</span></span>

[<span data-ttu-id="0b30e-138">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="0b30e-138">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="0b30e-139">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="0b30e-139">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="0b30e-140">Neu – AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="0b30e-140">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="0b30e-141">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="0b30e-141">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="0b30e-142">Satz-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="0b30e-142">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


