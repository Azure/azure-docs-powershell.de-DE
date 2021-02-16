---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppCertificate.md
ms.openlocfilehash: 56f8d69325e5a7918668ac2807449f348e73c91b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149681"
---
# <span data-ttu-id="85612-101">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="85612-101">New-AzWebAppCertificate</span></span>

## <span data-ttu-id="85612-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85612-102">SYNOPSIS</span></span>
<span data-ttu-id="85612-103">Erstellt ein vom App-Dienst verwaltetes Zertifikat für eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="85612-103">Creates an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="85612-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85612-104">SYNTAX</span></span>

```
New-AzWebAppCertificate [-ResourceGroupName] <String> [-WebAppName] <String> [-Name] <String> [[-Slot] <String>]
 [-HostName] <String> [-AddBinding] [[-SslState] <SslState>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85612-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85612-105">DESCRIPTION</span></span>
<span data-ttu-id="85612-106">Das **Cmdlet "New-AzWebAppCertificate"** erstellt ein verwaltetes Zertifikat für den Azure-App-Dienst.</span><span class="sxs-lookup"><span data-stu-id="85612-106">The **New-AzWebAppCertificate** cmdlet creates an Azure App Service Managed Certificate</span></span>
## <span data-ttu-id="85612-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="85612-107">EXAMPLES</span></span>

### <span data-ttu-id="85612-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="85612-108">Example 1</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net"
```

<span data-ttu-id="85612-109">Mit diesem Befehl wird ein vom App-Dienst verwaltetes Zertifikat für die angegebene WebApp erstellt.</span><span class="sxs-lookup"><span data-stu-id="85612-109">This command create an App Service Managed Certificate for the given WebApp</span></span>

### <span data-ttu-id="85612-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="85612-110">Example 2</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net" -Slot "test" -AddCertBinding
```

<span data-ttu-id="85612-111">Mit diesem Befehl wird ein vom App-Dienst verwaltetes Zertifikat erstellt und an das angegebene WebApp-Slot gebunden.</span><span class="sxs-lookup"><span data-stu-id="85612-111">This command create an App Service Managed Certificate and binds to the given WebApp Slot.</span></span>

### <span data-ttu-id="85612-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="85612-112">Example 3</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net" -AddBinding
```

<span data-ttu-id="85612-113">Mit diesem Befehl wird ein vom App Service verwaltetes Zertifikat erstellt und an die angegebene WebApp gebunden.</span><span class="sxs-lookup"><span data-stu-id="85612-113">This command create an App Service Managed Certificate and binds to the given WebApp.</span></span>

## <span data-ttu-id="85612-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85612-114">PARAMETERS</span></span>

### <span data-ttu-id="85612-115">-AddBinding</span><span class="sxs-lookup"><span data-stu-id="85612-115">-AddBinding</span></span>
<span data-ttu-id="85612-116">So fügen Sie das erstellte Zertifikat zu WebApp/Slot hinzu.</span><span class="sxs-lookup"><span data-stu-id="85612-116">To add the created certificate to WebApp/slot.</span></span>

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

### <span data-ttu-id="85612-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85612-117">-DefaultProfile</span></span>
<span data-ttu-id="85612-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85612-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85612-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="85612-119">-HostName</span></span>
<span data-ttu-id="85612-120">Benutzerdefinierte Hostnamen, die web app/slot zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="85612-120">Custom hostnames associated with web app/slot.</span></span>

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

### <span data-ttu-id="85612-121">-Name</span><span class="sxs-lookup"><span data-stu-id="85612-121">-Name</span></span>
<span data-ttu-id="85612-122">Der Name des Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="85612-122">The name of the certificate.</span></span>

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

### <span data-ttu-id="85612-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85612-123">-ResourceGroupName</span></span>
<span data-ttu-id="85612-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="85612-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="85612-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="85612-125">-Slot</span></span>
<span data-ttu-id="85612-126">Der Name des Web-App-Slot.</span><span class="sxs-lookup"><span data-stu-id="85612-126">The name of the web app slot.</span></span>

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

### <span data-ttu-id="85612-127">-SslState</span><span class="sxs-lookup"><span data-stu-id="85612-127">-SslState</span></span>
<span data-ttu-id="85612-128">Option "Ssl-Status".</span><span class="sxs-lookup"><span data-stu-id="85612-128">Ssl state option.</span></span>
<span data-ttu-id="85612-129">Verwenden Sie entweder "SniEnabled" oder "IpBasedEnabled".</span><span class="sxs-lookup"><span data-stu-id="85612-129">Use either 'SniEnabled' or 'IpBasedEnabled'.</span></span>
<span data-ttu-id="85612-130">Die Standardoption ist "SniEnabled".</span><span class="sxs-lookup"><span data-stu-id="85612-130">Default option is 'SniEnabled'.</span></span>

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

### <span data-ttu-id="85612-131">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="85612-131">-WebAppName</span></span>
<span data-ttu-id="85612-132">Der Name der Web App.</span><span class="sxs-lookup"><span data-stu-id="85612-132">The name of the web app.</span></span>

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

### <span data-ttu-id="85612-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85612-133">CommonParameters</span></span>
<span data-ttu-id="85612-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85612-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85612-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85612-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85612-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="85612-136">INPUTS</span></span>

### <span data-ttu-id="85612-137">Keine</span><span class="sxs-lookup"><span data-stu-id="85612-137">None</span></span>

## <span data-ttu-id="85612-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="85612-138">OUTPUTS</span></span>

### <span data-ttu-id="85612-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="85612-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="85612-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="85612-140">NOTES</span></span>

## <span data-ttu-id="85612-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="85612-141">RELATED LINKS</span></span>
[<span data-ttu-id="85612-142">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="85612-142">Remove-AzWebAppCertificate</span></span>](./Remove-AzWebAppCertificate.md)