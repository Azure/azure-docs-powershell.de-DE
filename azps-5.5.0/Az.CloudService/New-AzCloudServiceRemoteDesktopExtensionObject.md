---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-azcloudserviceremotedesktopextensionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
ms.openlocfilehash: 022093b8fe1df28a151405a18009b40dd24b0c97
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166652"
---
# <span data-ttu-id="fc149-101">New-AzCloudServiceRemoteDesktopExtensionObject</span><span class="sxs-lookup"><span data-stu-id="fc149-101">New-AzCloudServiceRemoteDesktopExtensionObject</span></span>

## <span data-ttu-id="fc149-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc149-102">SYNOPSIS</span></span>
<span data-ttu-id="fc149-103">Erstellen eines Speicherobjekts für die Remotedesktoperweiterung</span><span class="sxs-lookup"><span data-stu-id="fc149-103">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="fc149-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc149-104">SYNTAX</span></span>

```
New-AzCloudServiceRemoteDesktopExtensionObject [-Name] <String> [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-TypeHandlerVersion] <String>] [[-RolesAppliedTo] <String[]>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="fc149-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc149-105">DESCRIPTION</span></span>
<span data-ttu-id="fc149-106">Erstellen eines Speicherobjekts für die Remotedesktoperweiterung</span><span class="sxs-lookup"><span data-stu-id="fc149-106">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="fc149-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fc149-107">EXAMPLES</span></span>

### <span data-ttu-id="fc149-108">Beispiel 1: Erstellen eines Remotedesktoperweiterungsobjekts</span><span class="sxs-lookup"><span data-stu-id="fc149-108">Example 1: Create remote desktop extension object</span></span>
```powershell
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $extension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'
```

<span data-ttu-id="fc149-109">Dieser Befehl erstellt ein Remotedesktoperweiterungsobjekt, das zum Erstellen oder Aktualisieren eines Clouddiensts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fc149-109">This command creates remote desktop extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="fc149-110">Weitere Details finden Sie unter "New-AzCloudService".</span><span class="sxs-lookup"><span data-stu-id="fc149-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="fc149-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc149-111">PARAMETERS</span></span>

### <span data-ttu-id="fc149-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="fc149-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="fc149-113">Nebenversion für automatisches Upgrade</span><span class="sxs-lookup"><span data-stu-id="fc149-113">Auto upgrade minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc149-114">-Credential</span><span class="sxs-lookup"><span data-stu-id="fc149-114">-Credential</span></span>
<span data-ttu-id="fc149-115">Anmeldeinformationen für die Remotedesktoperweiterung.</span><span class="sxs-lookup"><span data-stu-id="fc149-115">Credential for Remote Desktop Extension.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc149-116">-Expiration</span><span class="sxs-lookup"><span data-stu-id="fc149-116">-Expiration</span></span>
<span data-ttu-id="fc149-117">Ablauf für Remotedesktoperweiterung.</span><span class="sxs-lookup"><span data-stu-id="fc149-117">Expiration for Remote Desktop Extension.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc149-118">-Name</span><span class="sxs-lookup"><span data-stu-id="fc149-118">-Name</span></span>
<span data-ttu-id="fc149-119">Name der Remotedesktoperweiterung.</span><span class="sxs-lookup"><span data-stu-id="fc149-119">Name of Remote Desktop Extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc149-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="fc149-120">-RolesAppliedTo</span></span>
<span data-ttu-id="fc149-121">Auf rollen angewendete Rollen.</span><span class="sxs-lookup"><span data-stu-id="fc149-121">Roles applied to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc149-122">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="fc149-122">-TypeHandlerVersion</span></span>
<span data-ttu-id="fc149-123">Version der Remotedesktoperweiterung.</span><span class="sxs-lookup"><span data-stu-id="fc149-123">Remote Desktop Extension version.</span></span>

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

### <span data-ttu-id="fc149-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc149-124">CommonParameters</span></span>
<span data-ttu-id="fc149-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc149-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc149-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc149-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc149-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fc149-127">INPUTS</span></span>

## <span data-ttu-id="fc149-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fc149-128">OUTPUTS</span></span>

### <span data-ttu-id="fc149-129">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="fc149-129">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="fc149-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fc149-130">NOTES</span></span>

<span data-ttu-id="fc149-131">ALIASE</span><span class="sxs-lookup"><span data-stu-id="fc149-131">ALIASES</span></span>

## <span data-ttu-id="fc149-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fc149-132">RELATED LINKS</span></span>

