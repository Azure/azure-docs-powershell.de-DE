---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/install-azakskubectl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
ms.openlocfilehash: 746efc579e1977e54a1898bbe183d951c3d9c21f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303242"
---
# <span data-ttu-id="cf745-101">Install-AzAksKubectl</span><span class="sxs-lookup"><span data-stu-id="cf745-101">Install-AzAksKubectl</span></span>

## <span data-ttu-id="cf745-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cf745-102">SYNOPSIS</span></span>
<span data-ttu-id="cf745-103">Laden Sie kubectl, das Kubernetes-Befehlszeilentool, herunter, und installieren Sie es.</span><span class="sxs-lookup"><span data-stu-id="cf745-103">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="cf745-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf745-104">SYNTAX</span></span>

```
Install-AzAksKubectl [-Destination <String>] [-Version <String>] [-DownloadFromMirror] [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf745-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf745-105">DESCRIPTION</span></span>
<span data-ttu-id="cf745-106">Laden Sie kubectl, das Kubernetes-Befehlszeilentool, herunter, und installieren Sie es.</span><span class="sxs-lookup"><span data-stu-id="cf745-106">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="cf745-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf745-107">EXAMPLES</span></span>

### <span data-ttu-id="cf745-108">Herunterladen und Installieren der neuesten Version von kubectl</span><span class="sxs-lookup"><span data-stu-id="cf745-108">Download and install latest version of kubectl</span></span>
```powershell
PS C:\> Install-AzAksKubectl -Version latest
```

## <span data-ttu-id="cf745-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf745-109">PARAMETERS</span></span>

### <span data-ttu-id="cf745-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf745-110">-AsJob</span></span>
<span data-ttu-id="cf745-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="cf745-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf745-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf745-112">-DefaultProfile</span></span>
<span data-ttu-id="cf745-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cf745-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf745-114">-Ziel</span><span class="sxs-lookup"><span data-stu-id="cf745-114">-Destination</span></span>
<span data-ttu-id="cf745-115">Der Pfad, auf dem kubectl installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf745-115">Path at which to install kubectl.</span></span>
<span data-ttu-id="cf745-116">Standardmäßige Installation in ~/.Azure-kubectl/</span><span class="sxs-lookup"><span data-stu-id="cf745-116">Default to install into ~/.azure-kubectl/</span></span>

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

### <span data-ttu-id="cf745-117">-DownloadFromMirror</span><span class="sxs-lookup"><span data-stu-id="cf745-117">-DownloadFromMirror</span></span>
<span data-ttu-id="cf745-118">Von Mirror-Website herunterladen: https://mirror.azure.cn/kubernetes/kubectl/</span><span class="sxs-lookup"><span data-stu-id="cf745-118">Download from mirror site : https://mirror.azure.cn/kubernetes/kubectl/</span></span>

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

### <span data-ttu-id="cf745-119">-Force</span><span class="sxs-lookup"><span data-stu-id="cf745-119">-Force</span></span>
<span data-ttu-id="cf745-120">Vorhandene kubectl ohne Eingabeaufforderung überschreiben</span><span class="sxs-lookup"><span data-stu-id="cf745-120">Overwrite existing kubectl without prompt</span></span>

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

### <span data-ttu-id="cf745-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf745-121">-PassThru</span></span>
<span data-ttu-id="cf745-122">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="cf745-122">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="cf745-123">-Version</span><span class="sxs-lookup"><span data-stu-id="cf745-123">-Version</span></span>
<span data-ttu-id="cf745-124">Die zu installierende Version von kubectl, beispielsweise "v 1.17.2".</span><span class="sxs-lookup"><span data-stu-id="cf745-124">Version of kubectl to install, e.g. 'v1.17.2'.</span></span>
<span data-ttu-id="cf745-125">Standardwert: aktuell</span><span class="sxs-lookup"><span data-stu-id="cf745-125">Default value: Latest</span></span>

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

### <span data-ttu-id="cf745-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cf745-126">-Confirm</span></span>
<span data-ttu-id="cf745-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cf745-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf745-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf745-128">-WhatIf</span></span>
<span data-ttu-id="cf745-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cf745-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf745-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf745-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf745-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf745-131">CommonParameters</span></span>
<span data-ttu-id="cf745-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf745-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf745-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf745-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf745-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cf745-134">INPUTS</span></span>

### <span data-ttu-id="cf745-135">Keine</span><span class="sxs-lookup"><span data-stu-id="cf745-135">None</span></span>

## <span data-ttu-id="cf745-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cf745-136">OUTPUTS</span></span>

### <span data-ttu-id="cf745-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf745-137">System.Boolean</span></span>

## <span data-ttu-id="cf745-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="cf745-138">NOTES</span></span>

## <span data-ttu-id="cf745-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cf745-139">RELATED LINKS</span></span>
