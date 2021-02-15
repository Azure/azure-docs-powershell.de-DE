---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/install-azakskubectl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
ms.openlocfilehash: 746efc579e1977e54a1898bbe183d951c3d9c21f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167084"
---
# <span data-ttu-id="93cd8-101">Install-AzAksKubectl</span><span class="sxs-lookup"><span data-stu-id="93cd8-101">Install-AzAksKubectl</span></span>

## <span data-ttu-id="93cd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="93cd8-103">Laden Sie "kubectl", das Befehlszeilentool "Kubernetes", herunter, und installieren Sie es.</span><span class="sxs-lookup"><span data-stu-id="93cd8-103">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="93cd8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93cd8-104">SYNTAX</span></span>

```
Install-AzAksKubectl [-Destination <String>] [-Version <String>] [-DownloadFromMirror] [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93cd8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="93cd8-105">DESCRIPTION</span></span>
<span data-ttu-id="93cd8-106">Laden Sie "kubectl", das Befehlszeilentool "Kubernetes", herunter, und installieren Sie es.</span><span class="sxs-lookup"><span data-stu-id="93cd8-106">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="93cd8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="93cd8-107">EXAMPLES</span></span>

### <span data-ttu-id="93cd8-108">Herunterladen und Installieren der neuesten Version von kubectl</span><span class="sxs-lookup"><span data-stu-id="93cd8-108">Download and install latest version of kubectl</span></span>
```powershell
PS C:\> Install-AzAksKubectl -Version latest
```

## <span data-ttu-id="93cd8-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93cd8-109">PARAMETERS</span></span>

### <span data-ttu-id="93cd8-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93cd8-110">-AsJob</span></span>
<span data-ttu-id="93cd8-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="93cd8-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93cd8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93cd8-112">-DefaultProfile</span></span>
<span data-ttu-id="93cd8-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93cd8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93cd8-114">-Destination</span><span class="sxs-lookup"><span data-stu-id="93cd8-114">-Destination</span></span>
<span data-ttu-id="93cd8-115">Pfad, unter dem "kubectl" installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="93cd8-115">Path at which to install kubectl.</span></span>
<span data-ttu-id="93cd8-116">Wird standardmäßig in ~/.azure-kubectl/ installiert.</span><span class="sxs-lookup"><span data-stu-id="93cd8-116">Default to install into ~/.azure-kubectl/</span></span>

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

### <span data-ttu-id="93cd8-117">-DownloadFromMirror</span><span class="sxs-lookup"><span data-stu-id="93cd8-117">-DownloadFromMirror</span></span>
<span data-ttu-id="93cd8-118">Von der Spiegelwebsite herunterladen: https://mirror.azure.cn/kubernetes/kubectl/</span><span class="sxs-lookup"><span data-stu-id="93cd8-118">Download from mirror site : https://mirror.azure.cn/kubernetes/kubectl/</span></span>

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

### <span data-ttu-id="93cd8-119">-Force</span><span class="sxs-lookup"><span data-stu-id="93cd8-119">-Force</span></span>
<span data-ttu-id="93cd8-120">Vorhandenes Kubectl ohne Eingabeaufforderung überschreiben</span><span class="sxs-lookup"><span data-stu-id="93cd8-120">Overwrite existing kubectl without prompt</span></span>

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

### <span data-ttu-id="93cd8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93cd8-121">-PassThru</span></span>
<span data-ttu-id="93cd8-122">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="93cd8-122">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="93cd8-123">-Version</span><span class="sxs-lookup"><span data-stu-id="93cd8-123">-Version</span></span>
<span data-ttu-id="93cd8-124">Version der zu installierende Kubectl, z. B. 'v1.17.2'.</span><span class="sxs-lookup"><span data-stu-id="93cd8-124">Version of kubectl to install, e.g. 'v1.17.2'.</span></span>
<span data-ttu-id="93cd8-125">Standardwert: Neueste</span><span class="sxs-lookup"><span data-stu-id="93cd8-125">Default value: Latest</span></span>

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

### <span data-ttu-id="93cd8-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93cd8-126">-Confirm</span></span>
<span data-ttu-id="93cd8-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="93cd8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93cd8-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="93cd8-128">-WhatIf</span></span>
<span data-ttu-id="93cd8-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="93cd8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93cd8-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="93cd8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93cd8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93cd8-131">CommonParameters</span></span>
<span data-ttu-id="93cd8-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93cd8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93cd8-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93cd8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93cd8-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="93cd8-134">INPUTS</span></span>

### <span data-ttu-id="93cd8-135">Keine</span><span class="sxs-lookup"><span data-stu-id="93cd8-135">None</span></span>

## <span data-ttu-id="93cd8-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="93cd8-136">OUTPUTS</span></span>

### <span data-ttu-id="93cd8-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="93cd8-137">System.Boolean</span></span>

## <span data-ttu-id="93cd8-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="93cd8-138">NOTES</span></span>

## <span data-ttu-id="93cd8-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="93cd8-139">RELATED LINKS</span></span>
