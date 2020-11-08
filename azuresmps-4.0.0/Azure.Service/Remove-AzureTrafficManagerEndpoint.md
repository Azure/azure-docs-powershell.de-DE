---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 50B83AEC-1B32-4089-9804-D388677C3F7E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7388841c48f2f7c6ba0752748b245cce1f8b5c4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006298"
---
# <span data-ttu-id="08aee-101">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="08aee-101">Remove-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="08aee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08aee-102">SYNOPSIS</span></span>
<span data-ttu-id="08aee-103">Entfernt einen Endpunkt aus einem Datenverkehrs-Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="08aee-103">Removes an endpoint from a Traffic Manager profile.</span></span>

## <span data-ttu-id="08aee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08aee-104">SYNTAX</span></span>

```
Remove-AzureTrafficManagerEndpoint -DomainName <String> [-Force]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="08aee-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08aee-105">DESCRIPTION</span></span>
<span data-ttu-id="08aee-106">Das Cmdlet **Remove-AzureTrafficManagerEndpoint** entfernt einen Endpunkt aus einem Microsoft Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="08aee-106">The **Remove-AzureTrafficManagerEndpoint** cmdlet removes an endpoint from a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="08aee-107">Nachdem Sie einen Endpunkt entfernt haben, übergeben Sie das Ergebnis mithilfe des Pipelineoperators an das Cmdlet " **Satz-AzureTrafficManagerProfile** ".</span><span class="sxs-lookup"><span data-stu-id="08aee-107">After you remove an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="08aee-108">Dieses Cmdlet stellt eine Verbindung mit Azure her, um Ihre Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="08aee-108">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="08aee-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08aee-109">EXAMPLES</span></span>

### <span data-ttu-id="08aee-110">Beispiel 1: Entfernen eines Endpunkts aus einem Profil</span><span class="sxs-lookup"><span data-stu-id="08aee-110">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Remove-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="08aee-111">Der erste Befehl verwendet das Cmdlet " **Get-AzureTrafficManagerProfile** ", um das Profil mit dem Namen ContosoProfile abzurufen, und speichert es dann in der $TrafficManagerProfile-Variablen.</span><span class="sxs-lookup"><span data-stu-id="08aee-111">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="08aee-112">Mit dem zweiten Befehl wird ein Endpunkt mit dem Domänennamen Contoso02App.cloudapp.net aus dem Profil des Datenverkehrs-Managers entfernt, das in $TrafficManagerProfile gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="08aee-112">The second command removes an endpoint that has the domain name Contoso02App.cloudapp.net from the Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="08aee-113">Der Befehl übergibt das Profilobjekt an das Cmdlet " **Satz-AzureTrafficManagerProfile** ", um die Verbindung zu Azure herzustellen, um Ihre Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="08aee-113">The command passes the profile object to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="08aee-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="08aee-114">PARAMETERS</span></span>

### <span data-ttu-id="08aee-115">-Domänenname</span><span class="sxs-lookup"><span data-stu-id="08aee-115">-DomainName</span></span>
<span data-ttu-id="08aee-116">Gibt den Domänennamen des zu entfernenden Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="08aee-116">Specifies the domain name of the endpoint to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08aee-117">-Force</span><span class="sxs-lookup"><span data-stu-id="08aee-117">-Force</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08aee-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="08aee-118">-Profile</span></span>
<span data-ttu-id="08aee-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="08aee-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="08aee-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="08aee-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="08aee-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="08aee-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="08aee-122">Gibt das Traffic Manager-Profilobjekt an, aus dem der Endpunkt entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="08aee-122">Specifies the Traffic Manager profile object from which to remove the endpoint.</span></span>

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08aee-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08aee-123">CommonParameters</span></span>
<span data-ttu-id="08aee-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08aee-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08aee-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08aee-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08aee-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08aee-126">INPUTS</span></span>

## <span data-ttu-id="08aee-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08aee-127">OUTPUTS</span></span>

### <span data-ttu-id="08aee-128">Microsoft. WindowsAzure. Commands. Utilities. Trafficmanager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="08aee-128">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="08aee-129">Dieses Cmdlet generiert ein Traffic Manager-Profilobjekt, das Informationen über das aktualisierte Profil enthält.</span><span class="sxs-lookup"><span data-stu-id="08aee-129">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="08aee-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="08aee-130">NOTES</span></span>

## <span data-ttu-id="08aee-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08aee-131">RELATED LINKS</span></span>

[<span data-ttu-id="08aee-132">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="08aee-132">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="08aee-133">Satz-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="08aee-133">Set-AzureTrafficManagerEndpoint</span></span>](./Set-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="08aee-134">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="08aee-134">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="08aee-135">Satz-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="08aee-135">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


