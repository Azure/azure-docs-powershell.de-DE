---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: aaecb97932ffbd2d7f5a03e4eedebd47719c5b4f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460447"
---
# <span data-ttu-id="7cc25-101">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="7cc25-101">Get-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="7cc25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cc25-102">SYNOPSIS</span></span>
<span data-ttu-id="7cc25-103">Ruft eine Azure Web App-Zertifikat-SSL-Bindung ab.</span><span class="sxs-lookup"><span data-stu-id="7cc25-103">Gets an Azure Web App certificate SSL binding.</span></span>

## <span data-ttu-id="7cc25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7cc25-104">SYNTAX</span></span>

### <span data-ttu-id="7cc25-105">S1</span><span class="sxs-lookup"><span data-stu-id="7cc25-105">S1</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cc25-106">S2</span><span class="sxs-lookup"><span data-stu-id="7cc25-106">S2</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7cc25-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7cc25-107">DESCRIPTION</span></span>
<span data-ttu-id="7cc25-108">Das **Cmdlet "Get-AzWebAppSSLBinding"** ruft eine Secure Sockets Layer (SSL)-Bindung für eine Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="7cc25-108">The **Get-AzWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="7cc25-109">SSL-Bindungen werden verwendet, um eine Web App einem hochgeladenen Zertifikat zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="7cc25-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="7cc25-110">Web Apps können an mehrere Zertifikate gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="7cc25-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="7cc25-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7cc25-111">EXAMPLES</span></span>

### <span data-ttu-id="7cc25-112">Beispiel 1: Erhalten von SSL-Bindungen für eine Web App</span><span class="sxs-lookup"><span data-stu-id="7cc25-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="7cc25-113">Mit diesem Befehl werden die SSL-Bindungen für die Web App ContosoWebApp abgerufen, die der Ressourcengruppe "ContosoResourceGroup" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7cc25-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="7cc25-114">Beispiel 2: Verwenden eines Objektverweises zum Erhalten von SSL-Bindungen für eine Web App</span><span class="sxs-lookup"><span data-stu-id="7cc25-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="7cc25-115">Die Befehle in diesem Beispiel erhalten auch die #A0 für die Web App ContosoWebApp. In diesem Fall wird jedoch anstelle des Web -App-Namens und des Namens der zugeordneten Ressourcengruppe ein Objektverweis verwendet.</span><span class="sxs-lookup"><span data-stu-id="7cc25-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="7cc25-116">Dieser Objektverweis wird durch den ersten Befehl im Beispiel erstellt, der **"Get-AzWebApp"** verwendet, um einen Objektverweis auf die Web App namens "ContosoWebApp" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7cc25-116">This object reference is created by the first command in the example, which uses **Get-AzWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="7cc25-117">Dieser Objektverweis wird in einer Variablen mit dem Namen $WebApp.</span><span class="sxs-lookup"><span data-stu-id="7cc25-117">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="7cc25-118">Diese Variable und das **Cmdlet "Get-AzWebAppSSLBinding"** werden dann vom zweiten Befehl verwendet, um die SSL-Bindungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7cc25-118">This variable, and the **Get-AzWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="7cc25-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cc25-119">PARAMETERS</span></span>

### <span data-ttu-id="7cc25-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cc25-120">-DefaultProfile</span></span>
<span data-ttu-id="7cc25-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7cc25-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cc25-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7cc25-122">-Name</span></span>
<span data-ttu-id="7cc25-123">Gibt den Namen der SSL-Bindung an.</span><span class="sxs-lookup"><span data-stu-id="7cc25-123">Specifies the name of the SSL binding.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cc25-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cc25-124">-ResourceGroupName</span></span>
<span data-ttu-id="7cc25-125">Gibt den Namen der Ressourcengruppe an, der das Zertifikat zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7cc25-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="7cc25-126">Sie können den Parameter *"ResourceGroupName"* und den Parameter *"WebApp" nicht* in demselben Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="7cc25-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cc25-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="7cc25-127">-Slot</span></span>
<span data-ttu-id="7cc25-128">Gibt einen Bereitstellungsplatz für Web App an.</span><span class="sxs-lookup"><span data-stu-id="7cc25-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="7cc25-129">Um einen Bereitstellungsplatz zu erhalten, verwenden Sie das Get-AzWebAppSlot Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cc25-129">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cc25-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7cc25-130">-WebApp</span></span>
<span data-ttu-id="7cc25-131">Gibt eine Web App an.</span><span class="sxs-lookup"><span data-stu-id="7cc25-131">Specifies a Web App.</span></span>
<span data-ttu-id="7cc25-132">Um eine Web App zu erhalten, verwenden Sie das Get-AzWebApp Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cc25-132">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cc25-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="7cc25-133">-WebAppName</span></span>
<span data-ttu-id="7cc25-134">Gibt den Namen der Web App an, aus der dieses Cmdlet SSL-Bindungen erhält.</span><span class="sxs-lookup"><span data-stu-id="7cc25-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>
<span data-ttu-id="7cc25-135">Sie können den Parameter *"WebAppName"* und den Parameter *"WebApp" nicht* im gleichen Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="7cc25-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cc25-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cc25-136">CommonParameters</span></span>
<span data-ttu-id="7cc25-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cc25-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cc25-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cc25-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cc25-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7cc25-139">INPUTS</span></span>

### <span data-ttu-id="7cc25-140">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="7cc25-140">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7cc25-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7cc25-141">OUTPUTS</span></span>

### <span data-ttu-id="7cc25-142">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="7cc25-142">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="7cc25-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7cc25-143">NOTES</span></span>

## <span data-ttu-id="7cc25-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7cc25-144">RELATED LINKS</span></span>

[<span data-ttu-id="7cc25-145">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="7cc25-145">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="7cc25-146">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="7cc25-146">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="7cc25-147">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7cc25-147">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


