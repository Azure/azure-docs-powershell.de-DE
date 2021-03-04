---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppCertificate.md
ms.openlocfilehash: 8e4ed309d4109ecfe230a522a65054213ae32049
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928784"
---
# <span data-ttu-id="60403-101">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="60403-101">New-AzWebAppCertificate</span></span>

## <span data-ttu-id="60403-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60403-102">SYNOPSIS</span></span>
<span data-ttu-id="60403-103">Erstellt ein vom App-Dienst verwaltetes Zertifikat für eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="60403-103">Creates an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="60403-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60403-104">SYNTAX</span></span>

```
New-AzWebAppCertificate [-ResourceGroupName] <String> [-WebAppName] <String> [-Name] <String> [[-Slot] <String>]
 [-HostName] <String> [-AddBinding] [[-SslState] <SslState>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60403-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60403-105">DESCRIPTION</span></span>
<span data-ttu-id="60403-106">Das **Cmdlet New-AzWebAppCertificate** erstellt ein verwaltetes Azure App Service-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="60403-106">The **New-AzWebAppCertificate** cmdlet creates an Azure App Service Managed Certificate</span></span>
## <span data-ttu-id="60403-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="60403-107">EXAMPLES</span></span>

### <span data-ttu-id="60403-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="60403-108">Example 1</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net"
```

<span data-ttu-id="60403-109">Mit diesem Befehl wird ein vom App Service verwaltetes Zertifikat für die angegebene WebApp erstellt.</span><span class="sxs-lookup"><span data-stu-id="60403-109">This command create an App Service Managed Certificate for the given WebApp</span></span>

### <span data-ttu-id="60403-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="60403-110">Example 2</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net" -Slot "test" -AddCertBinding
```

<span data-ttu-id="60403-111">Mit diesem Befehl wird ein vom App Service verwaltetes Zertifikat erstellt und an den angegebenen WebApp-Slot gebunden.</span><span class="sxs-lookup"><span data-stu-id="60403-111">This command create an App Service Managed Certificate and binds to the given WebApp Slot.</span></span>

### <span data-ttu-id="60403-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="60403-112">Example 3</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net" -AddBinding
```

<span data-ttu-id="60403-113">Mit diesem Befehl wird ein vom App Service verwaltetes Zertifikat erstellt und an die angegebene WebApp gebunden.</span><span class="sxs-lookup"><span data-stu-id="60403-113">This command create an App Service Managed Certificate and binds to the given WebApp.</span></span>

## <span data-ttu-id="60403-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="60403-114">PARAMETERS</span></span>

### <span data-ttu-id="60403-115">-AddBinding</span><span class="sxs-lookup"><span data-stu-id="60403-115">-AddBinding</span></span>
<span data-ttu-id="60403-116">So fügen Sie das erstellte Zertifikat zu WebApp/slot hinzu.</span><span class="sxs-lookup"><span data-stu-id="60403-116">To add the created certificate to WebApp/slot.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60403-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60403-117">-DefaultProfile</span></span>
<span data-ttu-id="60403-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60403-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60403-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="60403-119">-HostName</span></span>
<span data-ttu-id="60403-120">Benutzerdefinierte Hostnamen, die web app/slot zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="60403-120">Custom hostnames associated with web app/slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60403-121">-Name</span><span class="sxs-lookup"><span data-stu-id="60403-121">-Name</span></span>
<span data-ttu-id="60403-122">Der Name des Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="60403-122">The name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60403-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60403-123">-ResourceGroupName</span></span>
<span data-ttu-id="60403-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="60403-124">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60403-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="60403-125">-Slot</span></span>
<span data-ttu-id="60403-126">Der Name des Web-App-Steckplatzes.</span><span class="sxs-lookup"><span data-stu-id="60403-126">The name of the web app slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60403-127">-SslState</span><span class="sxs-lookup"><span data-stu-id="60403-127">-SslState</span></span>
<span data-ttu-id="60403-128">Ssl-Statusoption.</span><span class="sxs-lookup"><span data-stu-id="60403-128">Ssl state option.</span></span>
<span data-ttu-id="60403-129">Verwenden Sie entweder "SniEnabled" oder "IpBasedEnabled".</span><span class="sxs-lookup"><span data-stu-id="60403-129">Use either 'SniEnabled' or 'IpBasedEnabled'.</span></span>
<span data-ttu-id="60403-130">Die Standardoption ist "SniEnabled".</span><span class="sxs-lookup"><span data-stu-id="60403-130">Default option is 'SniEnabled'.</span></span>

```yaml
Type: SslState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60403-131">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="60403-131">-WebAppName</span></span>
<span data-ttu-id="60403-132">Der Name der Web App.</span><span class="sxs-lookup"><span data-stu-id="60403-132">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60403-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60403-133">CommonParameters</span></span>
<span data-ttu-id="60403-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60403-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60403-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60403-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60403-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="60403-136">INPUTS</span></span>

### <span data-ttu-id="60403-137">Keine</span><span class="sxs-lookup"><span data-stu-id="60403-137">None</span></span>

## <span data-ttu-id="60403-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="60403-138">OUTPUTS</span></span>

### <span data-ttu-id="60403-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="60403-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="60403-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="60403-140">NOTES</span></span>

## <span data-ttu-id="60403-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="60403-141">RELATED LINKS</span></span>
[<span data-ttu-id="60403-142">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="60403-142">Remove-AzWebAppCertificate</span></span>](./Remove-AzWebAppCertificate.md)