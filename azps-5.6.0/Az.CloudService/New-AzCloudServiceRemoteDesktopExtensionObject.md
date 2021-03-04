---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-azcloudserviceremotedesktopextensionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
ms.openlocfilehash: 5ae7383f71524c87518b9f48cbb314bf74de633e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942712"
---
# <span data-ttu-id="fc20c-101">New-AzCloudServiceRemoteDesktopExtensionObject</span><span class="sxs-lookup"><span data-stu-id="fc20c-101">New-AzCloudServiceRemoteDesktopExtensionObject</span></span>

## <span data-ttu-id="fc20c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc20c-102">SYNOPSIS</span></span>
<span data-ttu-id="fc20c-103">Erstellen eines Speicherobjekts für die Remotedesktoperweiterung</span><span class="sxs-lookup"><span data-stu-id="fc20c-103">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="fc20c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc20c-104">SYNTAX</span></span>

```
New-AzCloudServiceRemoteDesktopExtensionObject [-Name] <String> [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-TypeHandlerVersion] <String>] [[-RolesAppliedTo] <String[]>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="fc20c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc20c-105">DESCRIPTION</span></span>
<span data-ttu-id="fc20c-106">Erstellen eines Speicherobjekts für die Remotedesktoperweiterung</span><span class="sxs-lookup"><span data-stu-id="fc20c-106">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="fc20c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fc20c-107">EXAMPLES</span></span>

### <span data-ttu-id="fc20c-108">Beispiel 1: Erstellen eines Remotedesktoperweiterungsobjekts</span><span class="sxs-lookup"><span data-stu-id="fc20c-108">Example 1: Create remote desktop extension object</span></span>
```powershell
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $extension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'
```

<span data-ttu-id="fc20c-109">Mit diesem Befehl wird ein Remotedesktoperweiterungsobjekt erstellt, das zum Erstellen oder Aktualisieren eines Clouddiensts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fc20c-109">This command creates remote desktop extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="fc20c-110">Weitere Informationen finden Sie unter New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="fc20c-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="fc20c-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fc20c-111">PARAMETERS</span></span>

### <span data-ttu-id="fc20c-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="fc20c-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="fc20c-113">Nebenversion für automatisches Upgrade.</span><span class="sxs-lookup"><span data-stu-id="fc20c-113">Auto upgrade minor version.</span></span>

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

### <span data-ttu-id="fc20c-114">-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="fc20c-114">-Credential</span></span>
<span data-ttu-id="fc20c-115">Anmeldeinformationen für die Remotedesktoperweiterung.</span><span class="sxs-lookup"><span data-stu-id="fc20c-115">Credential for Remote Desktop Extension.</span></span>

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

### <span data-ttu-id="fc20c-116">-Expiration</span><span class="sxs-lookup"><span data-stu-id="fc20c-116">-Expiration</span></span>
<span data-ttu-id="fc20c-117">Ablauf für Remotedesktoperweiterung.</span><span class="sxs-lookup"><span data-stu-id="fc20c-117">Expiration for Remote Desktop Extension.</span></span>

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

### <span data-ttu-id="fc20c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="fc20c-118">-Name</span></span>
<span data-ttu-id="fc20c-119">Name der Remotedesktoperweiterung.</span><span class="sxs-lookup"><span data-stu-id="fc20c-119">Name of Remote Desktop Extension.</span></span>

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

### <span data-ttu-id="fc20c-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="fc20c-120">-RolesAppliedTo</span></span>
<span data-ttu-id="fc20c-121">Auf angewendete Rollen.</span><span class="sxs-lookup"><span data-stu-id="fc20c-121">Roles applied to.</span></span>

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

### <span data-ttu-id="fc20c-122">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="fc20c-122">-TypeHandlerVersion</span></span>
<span data-ttu-id="fc20c-123">Remotedesktoperweiterungsversion.</span><span class="sxs-lookup"><span data-stu-id="fc20c-123">Remote Desktop Extension version.</span></span>

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

### <span data-ttu-id="fc20c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc20c-124">CommonParameters</span></span>
<span data-ttu-id="fc20c-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc20c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc20c-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc20c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc20c-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fc20c-127">INPUTS</span></span>

## <span data-ttu-id="fc20c-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fc20c-128">OUTPUTS</span></span>

### <span data-ttu-id="fc20c-129">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="fc20c-129">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="fc20c-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fc20c-130">NOTES</span></span>

<span data-ttu-id="fc20c-131">ALIASE</span><span class="sxs-lookup"><span data-stu-id="fc20c-131">ALIASES</span></span>

## <span data-ttu-id="fc20c-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fc20c-132">RELATED LINKS</span></span>

