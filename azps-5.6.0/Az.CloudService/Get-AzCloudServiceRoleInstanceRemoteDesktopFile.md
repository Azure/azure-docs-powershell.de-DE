---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-azcloudserviceroleinstanceremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md
ms.openlocfilehash: 74948fe91e4a2823c9bbe8e8c0e50ade33612e18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938987"
---
# <span data-ttu-id="49b1d-101">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="49b1d-101">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span></span>

## <span data-ttu-id="49b1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49b1d-102">SYNOPSIS</span></span>
<span data-ttu-id="49b1d-103">Ruft eine Remotedesktopdatei für eine Rolleninstanz in einem Clouddienst ab.</span><span class="sxs-lookup"><span data-stu-id="49b1d-103">Gets a remote desktop file for a role instance in a cloud service.</span></span>

## <span data-ttu-id="49b1d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49b1d-104">SYNTAX</span></span>

```
Get-AzCloudServiceRoleInstanceRemoteDesktopFile -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> -OutFile <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

## <span data-ttu-id="49b1d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49b1d-105">DESCRIPTION</span></span>
<span data-ttu-id="49b1d-106">Ruft eine Remotedesktopdatei für eine Rolleninstanz in einem Clouddienst ab.</span><span class="sxs-lookup"><span data-stu-id="49b1d-106">Gets a remote desktop file for a role instance in a cloud service.</span></span>

## <span data-ttu-id="49b1d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="49b1d-107">EXAMPLES</span></span>

### <span data-ttu-id="49b1d-108">Beispiel 1: Herunterladen einer RDP-Datei</span><span class="sxs-lookup"><span data-stu-id="49b1d-108">Example 1: Get an RDP file</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstanceRemoteDesktopFile -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0" -OutFile "C:\temp\ContosoFrontEnd_IN_0.rdp"
```

<span data-ttu-id="49b1d-109">Dieser Befehl ruft eine RDP-Datei für die Rolleninstanz namens ContosoFrontEnd IN 0 des Clouddiensts contosoCS ab, die zur Ressourcengruppe \_ \_ "ContosOrg" gehört.</span><span class="sxs-lookup"><span data-stu-id="49b1d-109">This command gets an RDP file for the role instance named ContosoFrontEnd\_IN\_0 of cloud Service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="49b1d-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="49b1d-110">PARAMETERS</span></span>

### <span data-ttu-id="49b1d-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="49b1d-111">-CloudServiceName</span></span>
<span data-ttu-id="49b1d-112">.</span><span class="sxs-lookup"><span data-stu-id="49b1d-112">.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49b1d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b1d-113">-DefaultProfile</span></span>
<span data-ttu-id="49b1d-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49b1d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49b1d-115">-OutFile</span><span class="sxs-lookup"><span data-stu-id="49b1d-115">-OutFile</span></span>
<span data-ttu-id="49b1d-116">Pfad zum Schreiben einer Ausgabedatei in</span><span class="sxs-lookup"><span data-stu-id="49b1d-116">Path to write output file to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49b1d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49b1d-117">-PassThru</span></span>
<span data-ttu-id="49b1d-118">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49b1d-118">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="49b1d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49b1d-119">-ResourceGroupName</span></span>
<span data-ttu-id="49b1d-120">.</span><span class="sxs-lookup"><span data-stu-id="49b1d-120">.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49b1d-121">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="49b1d-121">-RoleInstanceName</span></span>
<span data-ttu-id="49b1d-122">Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="49b1d-122">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49b1d-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49b1d-123">-SubscriptionId</span></span>
<span data-ttu-id="49b1d-124">Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="49b1d-124">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="49b1d-125">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="49b1d-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49b1d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b1d-126">CommonParameters</span></span>
<span data-ttu-id="49b1d-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49b1d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b1d-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49b1d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b1d-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="49b1d-129">INPUTS</span></span>

## <span data-ttu-id="49b1d-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="49b1d-130">OUTPUTS</span></span>

### <span data-ttu-id="49b1d-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="49b1d-131">System.Boolean</span></span>

## <span data-ttu-id="49b1d-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="49b1d-132">NOTES</span></span>

<span data-ttu-id="49b1d-133">ALIASE</span><span class="sxs-lookup"><span data-stu-id="49b1d-133">ALIASES</span></span>

## <span data-ttu-id="49b1d-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="49b1d-134">RELATED LINKS</span></span>

