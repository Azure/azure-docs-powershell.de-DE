---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
ms.openlocfilehash: 12603400c3d1f29eaf77d9a279d7510e08b9fe5d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939803"
---
# <span data-ttu-id="bbe12-101">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="bbe12-101">Get-AzWebAppCertificate</span></span>

## <span data-ttu-id="bbe12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbe12-102">SYNOPSIS</span></span>
<span data-ttu-id="bbe12-103">Ruft ein Azure Web App-Zertifikat ab.</span><span class="sxs-lookup"><span data-stu-id="bbe12-103">Gets an Azure Web App certificate.</span></span>

## <span data-ttu-id="bbe12-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bbe12-104">SYNTAX</span></span>

```
Get-AzWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbe12-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bbe12-105">DESCRIPTION</span></span>
<span data-ttu-id="bbe12-106">Das **Get-AzWebAppCertificate-Cmdlet** ruft Informationen zu Azure Web App-Zertifikaten ab, die einer angegebenen Ressourcengruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bbe12-106">The **Get-AzWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="bbe12-107">Wenn Sie den Fingerabdruck des Zertifikats kennen, können Sie dieses Cmdlet auch verwenden, um Informationen zu einem angegebenen Zertifikat zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bbe12-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="bbe12-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bbe12-108">EXAMPLES</span></span>

### <span data-ttu-id="bbe12-109">Beispiel 1: Herunterladen von Web App-Zertifikaten in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="bbe12-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="bbe12-110">Dieser Befehl gibt Informationen zu den hochgeladenen Web App-Zertifikaten zurück, die der Ressourcengruppe ContosoResourceGroup zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bbe12-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="bbe12-111">Beispiel 2: Erhalten eines angegebenen Web App-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="bbe12-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="bbe12-112">Dieser Befehl ruft das ContosoResourceGroup Web App-Zertifikat mit dem Fingerabdruck E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 ab.</span><span class="sxs-lookup"><span data-stu-id="bbe12-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="bbe12-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bbe12-113">PARAMETERS</span></span>

### <span data-ttu-id="bbe12-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbe12-114">-DefaultProfile</span></span>
<span data-ttu-id="bbe12-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bbe12-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbe12-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbe12-116">-ResourceGroupName</span></span>
<span data-ttu-id="bbe12-117">Gibt den Namen der Ressourcengruppe an, der das Zertifikat zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="bbe12-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe12-118">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="bbe12-118">-Thumbprint</span></span>
<span data-ttu-id="bbe12-119">Gibt den eindeutigen Bezeichner für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="bbe12-119">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe12-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbe12-120">CommonParameters</span></span>
<span data-ttu-id="bbe12-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbe12-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbe12-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbe12-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbe12-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bbe12-123">INPUTS</span></span>

### <span data-ttu-id="bbe12-124">Keine</span><span class="sxs-lookup"><span data-stu-id="bbe12-124">None</span></span>

## <span data-ttu-id="bbe12-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bbe12-125">OUTPUTS</span></span>

### <span data-ttu-id="bbe12-126">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="bbe12-126">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="bbe12-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bbe12-127">NOTES</span></span>

## <span data-ttu-id="bbe12-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bbe12-128">RELATED LINKS</span></span>

[<span data-ttu-id="bbe12-129">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="bbe12-129">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)


