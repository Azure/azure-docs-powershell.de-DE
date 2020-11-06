---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 7f3849e1cabcd2fc838255bb312f5bfe5959e088
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499113"
---
# <span data-ttu-id="ed55b-101">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ed55b-101">Enable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="ed55b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed55b-102">SYNOPSIS</span></span>
<span data-ttu-id="ed55b-103">Aktiviert ein Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="ed55b-103">Enables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed55b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed55b-104">SYNTAX</span></span>

### <span data-ttu-id="ed55b-105">Felder</span><span class="sxs-lookup"><span data-stu-id="ed55b-105">Fields</span></span>
```
Enable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed55b-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="ed55b-106">Object</span></span>
```
Enable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed55b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed55b-107">DESCRIPTION</span></span>
<span data-ttu-id="ed55b-108">Das Cmdlet **enable-AzureRmTrafficManagerProfile** aktiviert ein Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="ed55b-108">The **Enable-AzureRmTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="ed55b-109">Sie können das Profilobjekt mithilfe der Pipeline oder als Parameterwert angeben.</span><span class="sxs-lookup"><span data-stu-id="ed55b-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="ed55b-110">Alternativ können Sie das Profil mithilfe der Parameter *Name* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="ed55b-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="ed55b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed55b-111">EXAMPLES</span></span>

### <span data-ttu-id="ed55b-112">Beispiel 1: Aktivieren eines durch den Namen angegebenen Profils</span><span class="sxs-lookup"><span data-stu-id="ed55b-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="ed55b-113">Dieser Befehl aktiviert das Profil mit dem Namen ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ed55b-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="ed55b-114">Beispiel 2: Aktivieren eines Profils mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="ed55b-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerProfile
```

<span data-ttu-id="ed55b-115">Dieser Befehl ruft das Profil mit dem Namen ContosoProfile in ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="ed55b-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="ed55b-116">Der Befehl übergibt dann dieses Profil mithilfe des Pipelineoperators an das Cmdlet **enable-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="ed55b-116">The command then passes that profile to the **Enable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ed55b-117">Dieses Cmdlet aktiviert dieses Profil.</span><span class="sxs-lookup"><span data-stu-id="ed55b-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="ed55b-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed55b-118">PARAMETERS</span></span>

### <span data-ttu-id="ed55b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ed55b-119">-Name</span></span>
<span data-ttu-id="ed55b-120">Gibt den Namen des Traffic Manager-Profils an, das dieses Cmdlet aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ed55b-120">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

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

### <span data-ttu-id="ed55b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed55b-121">-ResourceGroupName</span></span>
<span data-ttu-id="ed55b-122">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ed55b-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ed55b-123">Dieses Cmdlet aktiviert ein Datenverkehrs-Manager-Profil in der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ed55b-123">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ed55b-124">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ed55b-124">-TrafficManagerProfile</span></span>
<span data-ttu-id="ed55b-125">Gibt ein **TrafficManagerProfile** -Objekt an, das aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed55b-125">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="ed55b-126">Verwenden Sie das Get-AzureRmTrafficManagerProfile-Cmdlet, um ein **TrafficManagerProfile** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ed55b-126">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="ed55b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed55b-127">-DefaultProfile</span></span>
<span data-ttu-id="ed55b-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ed55b-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed55b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed55b-129">CommonParameters</span></span>
<span data-ttu-id="ed55b-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed55b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed55b-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed55b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed55b-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed55b-132">INPUTS</span></span>

### <span data-ttu-id="ed55b-133">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ed55b-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="ed55b-134">Dieses Cmdlet akzeptiert ein **TrafficManagerProfile** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="ed55b-134">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="ed55b-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed55b-135">OUTPUTS</span></span>

### <span data-ttu-id="ed55b-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ed55b-136">System.Boolean</span></span>

## <span data-ttu-id="ed55b-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed55b-137">NOTES</span></span>

## <span data-ttu-id="ed55b-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed55b-138">RELATED LINKS</span></span>

[<span data-ttu-id="ed55b-139">Deaktivieren-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ed55b-139">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="ed55b-140">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ed55b-140">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="ed55b-141">Neu – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ed55b-141">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="ed55b-142">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ed55b-142">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="ed55b-143">Satz-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ed55b-143">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


