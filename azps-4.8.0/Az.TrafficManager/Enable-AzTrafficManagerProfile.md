---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
ms.openlocfilehash: ba578d800631304405ab1e0a4139a11d9f2a26dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174876"
---
# <span data-ttu-id="5c933-101">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c933-101">Enable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="5c933-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5c933-102">SYNOPSIS</span></span>
<span data-ttu-id="5c933-103">Aktiviert ein Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="5c933-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="5c933-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c933-104">SYNTAX</span></span>

### <span data-ttu-id="5c933-105">Felder</span><span class="sxs-lookup"><span data-stu-id="5c933-105">Fields</span></span>
```
Enable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c933-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="5c933-106">Object</span></span>
```
Enable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c933-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c933-107">DESCRIPTION</span></span>
<span data-ttu-id="5c933-108">Das Cmdlet **enable-AzTrafficManagerProfile** aktiviert ein Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="5c933-108">The **Enable-AzTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="5c933-109">Sie können das Profilobjekt mithilfe der Pipeline oder als Parameterwert angeben.</span><span class="sxs-lookup"><span data-stu-id="5c933-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="5c933-110">Alternativ können Sie das Profil mithilfe der Parameter *Name* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="5c933-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="5c933-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5c933-111">EXAMPLES</span></span>

### <span data-ttu-id="5c933-112">Beispiel 1: Aktivieren eines durch den Namen angegebenen Profils</span><span class="sxs-lookup"><span data-stu-id="5c933-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="5c933-113">Dieser Befehl aktiviert das Profil mit dem Namen ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="5c933-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="5c933-114">Beispiel 2: Aktivieren eines Profils mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="5c933-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerProfile
```

<span data-ttu-id="5c933-115">Dieser Befehl ruft das Profil mit dem Namen ContosoProfile in ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="5c933-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="5c933-116">Der Befehl übergibt dann dieses Profil mithilfe des Pipelineoperators an das Cmdlet **enable-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="5c933-116">The command then passes that profile to the **Enable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5c933-117">Dieses Cmdlet aktiviert dieses Profil.</span><span class="sxs-lookup"><span data-stu-id="5c933-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="5c933-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c933-118">PARAMETERS</span></span>

### <span data-ttu-id="5c933-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c933-119">-DefaultProfile</span></span>
<span data-ttu-id="5c933-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5c933-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c933-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5c933-121">-Name</span></span>
<span data-ttu-id="5c933-122">Gibt den Namen des Traffic Manager-Profils an, das dieses Cmdlet aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5c933-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c933-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c933-123">-ResourceGroupName</span></span>
<span data-ttu-id="5c933-124">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="5c933-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="5c933-125">Dieses Cmdlet aktiviert ein Datenverkehrs-Manager-Profil in der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5c933-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c933-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c933-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="5c933-127">Gibt ein **TrafficManagerProfile** -Objekt an, das aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c933-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="5c933-128">Verwenden Sie das Get-AzTrafficManagerProfile-Cmdlet, um ein **TrafficManagerProfile** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5c933-128">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c933-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c933-129">CommonParameters</span></span>
<span data-ttu-id="5c933-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c933-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c933-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c933-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c933-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5c933-132">INPUTS</span></span>

### <span data-ttu-id="5c933-133">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c933-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="5c933-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5c933-134">OUTPUTS</span></span>

### <span data-ttu-id="5c933-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5c933-135">System.Boolean</span></span>

## <span data-ttu-id="5c933-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="5c933-136">NOTES</span></span>

## <span data-ttu-id="5c933-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5c933-137">RELATED LINKS</span></span>

[<span data-ttu-id="5c933-138">Deaktivieren-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c933-138">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="5c933-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c933-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="5c933-140">Neu – AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c933-140">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="5c933-141">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c933-141">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="5c933-142">Satz-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c933-142">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


