---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
ms.openlocfilehash: 7988975daa512b44c71b17929f47d3318bfe192c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149665"
---
# <span data-ttu-id="6a8dc-101">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="6a8dc-101">Remove-AzWebAppCertificate</span></span>

## <span data-ttu-id="6a8dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a8dc-102">SYNOPSIS</span></span>
<span data-ttu-id="6a8dc-103">Erstellt ein vom App-Dienst verwaltetes Zertifikat für eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="6a8dc-103">Creates an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="6a8dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a8dc-104">SYNTAX</span></span>

```
Remove-AzWebAppCertificate [-ResourceGroupName] <String> [-ThumbPrint] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a8dc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a8dc-105">DESCRIPTION</span></span>
<span data-ttu-id="6a8dc-106">Das **Cmdlet "Remove-AzWebAppCertificate"** erstellt ein verwaltetes Zertifikat für den Azure-App-Dienst.</span><span class="sxs-lookup"><span data-stu-id="6a8dc-106">The **Remove-AzWebAppCertificate** cmdlet creates an Azure App Service Managed Certificate</span></span>

## <span data-ttu-id="6a8dc-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6a8dc-107">EXAMPLES</span></span>

### <span data-ttu-id="6a8dc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6a8dc-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" 
```

<span data-ttu-id="6a8dc-109">Mit diesem Befehl wird das vom App-Dienst verwaltete Zertifikat für die angegebene Web App entfernt.</span><span class="sxs-lookup"><span data-stu-id="6a8dc-109">This command removes App Service Managed certificate for the given web app.</span></span>

## <span data-ttu-id="6a8dc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a8dc-110">PARAMETERS</span></span>

### <span data-ttu-id="6a8dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a8dc-111">-DefaultProfile</span></span>
<span data-ttu-id="6a8dc-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a8dc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a8dc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a8dc-113">-ResourceGroupName</span></span>
<span data-ttu-id="6a8dc-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6a8dc-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="6a8dc-115">-ThumbPrint</span><span class="sxs-lookup"><span data-stu-id="6a8dc-115">-ThumbPrint</span></span>
<span data-ttu-id="6a8dc-116">Fingerabdruck des Zertifikats, das bereits im Webbereich vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6a8dc-116">Thumbprint of the certificate that already exists in web space.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a8dc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a8dc-117">CommonParameters</span></span>
<span data-ttu-id="6a8dc-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a8dc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a8dc-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a8dc-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a8dc-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6a8dc-120">INPUTS</span></span>

### <span data-ttu-id="6a8dc-121">Keine</span><span class="sxs-lookup"><span data-stu-id="6a8dc-121">None</span></span>

## <span data-ttu-id="6a8dc-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6a8dc-122">OUTPUTS</span></span>

### <span data-ttu-id="6a8dc-123">System.Void</span><span class="sxs-lookup"><span data-stu-id="6a8dc-123">System.Void</span></span>

## <span data-ttu-id="6a8dc-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6a8dc-124">NOTES</span></span>

## <span data-ttu-id="6a8dc-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6a8dc-125">RELATED LINKS</span></span>
[<span data-ttu-id="6a8dc-126">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="6a8dc-126">New-AzWebAppCertificate</span></span>](./New-AzWebAppCertificate.md)
