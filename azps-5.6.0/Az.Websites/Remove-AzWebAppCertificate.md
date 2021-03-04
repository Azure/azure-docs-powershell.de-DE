---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
ms.openlocfilehash: adea8ace20b5e7c3c3c8d28161de53afdb431e19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933475"
---
# <span data-ttu-id="47c62-101">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="47c62-101">Remove-AzWebAppCertificate</span></span>

## <span data-ttu-id="47c62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47c62-102">SYNOPSIS</span></span>
<span data-ttu-id="47c62-103">Entfernt ein vom App-Dienst verwaltetes Zertifikat für eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="47c62-103">Removes an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="47c62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47c62-104">SYNTAX</span></span>

```
Remove-AzWebAppCertificate [-ResourceGroupName] <String> [-ThumbPrint] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47c62-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47c62-105">DESCRIPTION</span></span>
<span data-ttu-id="47c62-106">Das **Cmdlet Remove-AzWebAppCertificate** entfernt ein verwaltetes Azure App Service-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="47c62-106">The **Remove-AzWebAppCertificate** cmdlet Removes an Azure App Service Managed Certificate</span></span>

## <span data-ttu-id="47c62-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="47c62-107">EXAMPLES</span></span>

### <span data-ttu-id="47c62-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="47c62-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" 
```

<span data-ttu-id="47c62-109">Mit diesem Befehl wird das vom App-Dienst verwaltete Zertifikat für die angegebene Web App entfernt.</span><span class="sxs-lookup"><span data-stu-id="47c62-109">This command removes App Service Managed certificate for the given web app.</span></span>

## <span data-ttu-id="47c62-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="47c62-110">PARAMETERS</span></span>

### <span data-ttu-id="47c62-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47c62-111">-DefaultProfile</span></span>
<span data-ttu-id="47c62-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47c62-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47c62-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47c62-113">-ResourceGroupName</span></span>
<span data-ttu-id="47c62-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="47c62-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="47c62-115">-ThumbPrint</span><span class="sxs-lookup"><span data-stu-id="47c62-115">-ThumbPrint</span></span>
<span data-ttu-id="47c62-116">Fingerabdruck des Zertifikats, das bereits im Webbereich vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="47c62-116">Thumbprint of the certificate that already exists in web space.</span></span>

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

### <span data-ttu-id="47c62-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47c62-117">CommonParameters</span></span>
<span data-ttu-id="47c62-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47c62-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47c62-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47c62-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47c62-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="47c62-120">INPUTS</span></span>

### <span data-ttu-id="47c62-121">Keine</span><span class="sxs-lookup"><span data-stu-id="47c62-121">None</span></span>

## <span data-ttu-id="47c62-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="47c62-122">OUTPUTS</span></span>

### <span data-ttu-id="47c62-123">System.Void</span><span class="sxs-lookup"><span data-stu-id="47c62-123">System.Void</span></span>

## <span data-ttu-id="47c62-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="47c62-124">NOTES</span></span>

## <span data-ttu-id="47c62-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="47c62-125">RELATED LINKS</span></span>
[<span data-ttu-id="47c62-126">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="47c62-126">New-AzWebAppCertificate</span></span>](./New-AzWebAppCertificate.md)
