---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/install-azakskubectl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
ms.openlocfilehash: 746efc579e1977e54a1898bbe183d951c3d9c21f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471563"
---
# <span data-ttu-id="f81d3-101">Install-AzAksKubectl</span><span class="sxs-lookup"><span data-stu-id="f81d3-101">Install-AzAksKubectl</span></span>

## <span data-ttu-id="f81d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f81d3-102">SYNOPSIS</span></span>
<span data-ttu-id="f81d3-103">Laden Sie "kubectl" herunter, und installieren Sie es, das Befehlszeilentool "Kubernetes".</span><span class="sxs-lookup"><span data-stu-id="f81d3-103">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="f81d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f81d3-104">SYNTAX</span></span>

```
Install-AzAksKubectl [-Destination <String>] [-Version <String>] [-DownloadFromMirror] [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f81d3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f81d3-105">DESCRIPTION</span></span>
<span data-ttu-id="f81d3-106">Laden Sie "kubectl" herunter, und installieren Sie es, das Befehlszeilentool "Kubernetes".</span><span class="sxs-lookup"><span data-stu-id="f81d3-106">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="f81d3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f81d3-107">EXAMPLES</span></span>

### <span data-ttu-id="f81d3-108">Herunterladen und Installieren der neuesten Version von kubectl</span><span class="sxs-lookup"><span data-stu-id="f81d3-108">Download and install latest version of kubectl</span></span>
```powershell
PS C:\> Install-AzAksKubectl -Version latest
```

## <span data-ttu-id="f81d3-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f81d3-109">PARAMETERS</span></span>

### <span data-ttu-id="f81d3-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f81d3-110">-AsJob</span></span>
<span data-ttu-id="f81d3-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f81d3-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f81d3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f81d3-112">-DefaultProfile</span></span>
<span data-ttu-id="f81d3-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f81d3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f81d3-114">-Destination</span><span class="sxs-lookup"><span data-stu-id="f81d3-114">-Destination</span></span>
<span data-ttu-id="f81d3-115">Pfad, unter dem "kubectl" installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f81d3-115">Path at which to install kubectl.</span></span>
<span data-ttu-id="f81d3-116">Wird standardmäßig in ~/.azure-kubectl/ installiert.</span><span class="sxs-lookup"><span data-stu-id="f81d3-116">Default to install into ~/.azure-kubectl/</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f81d3-117">-DownloadFromMirror</span><span class="sxs-lookup"><span data-stu-id="f81d3-117">-DownloadFromMirror</span></span>
<span data-ttu-id="f81d3-118">Download von der Mirror-Website: https://mirror.azure.cn/kubernetes/kubectl/</span><span class="sxs-lookup"><span data-stu-id="f81d3-118">Download from mirror site : https://mirror.azure.cn/kubernetes/kubectl/</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f81d3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f81d3-119">-Force</span></span>
<span data-ttu-id="f81d3-120">Vorhandenes Kubectl ohne Eingabeaufforderung überschreiben</span><span class="sxs-lookup"><span data-stu-id="f81d3-120">Overwrite existing kubectl without prompt</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f81d3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f81d3-121">-PassThru</span></span>
<span data-ttu-id="f81d3-122">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="f81d3-122">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f81d3-123">-Version</span><span class="sxs-lookup"><span data-stu-id="f81d3-123">-Version</span></span>
<span data-ttu-id="f81d3-124">Version der zu installierende Kubectl, z. B. 'v1.17.2'.</span><span class="sxs-lookup"><span data-stu-id="f81d3-124">Version of kubectl to install, e.g. 'v1.17.2'.</span></span>
<span data-ttu-id="f81d3-125">Standardwert: Neueste</span><span class="sxs-lookup"><span data-stu-id="f81d3-125">Default value: Latest</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f81d3-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f81d3-126">-Confirm</span></span>
<span data-ttu-id="f81d3-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f81d3-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f81d3-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f81d3-128">-WhatIf</span></span>
<span data-ttu-id="f81d3-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f81d3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f81d3-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f81d3-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f81d3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f81d3-131">CommonParameters</span></span>
<span data-ttu-id="f81d3-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f81d3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f81d3-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f81d3-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f81d3-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f81d3-134">INPUTS</span></span>

### <span data-ttu-id="f81d3-135">Keine</span><span class="sxs-lookup"><span data-stu-id="f81d3-135">None</span></span>

## <span data-ttu-id="f81d3-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f81d3-136">OUTPUTS</span></span>

### <span data-ttu-id="f81d3-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f81d3-137">System.Boolean</span></span>

## <span data-ttu-id="f81d3-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f81d3-138">NOTES</span></span>

## <span data-ttu-id="f81d3-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f81d3-139">RELATED LINKS</span></span>
