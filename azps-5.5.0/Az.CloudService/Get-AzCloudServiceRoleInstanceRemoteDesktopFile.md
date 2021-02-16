---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceroleinstanceremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md
ms.openlocfilehash: 2b4133942a3aa7c4e9339579465942ade96c5709
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149028"
---
# <span data-ttu-id="a485c-101">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="a485c-101">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span></span>

## <span data-ttu-id="a485c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a485c-102">SYNOPSIS</span></span>
<span data-ttu-id="a485c-103">Ruft eine Remotedesktopdatei für eine Rolleninstanz in einem Clouddienst ab.</span><span class="sxs-lookup"><span data-stu-id="a485c-103">Gets a remote desktop file for a role instance in a cloud service.</span></span>

## <span data-ttu-id="a485c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a485c-104">SYNTAX</span></span>

```
Get-AzCloudServiceRoleInstanceRemoteDesktopFile -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> -OutFile <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

## <span data-ttu-id="a485c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a485c-105">DESCRIPTION</span></span>
<span data-ttu-id="a485c-106">Ruft eine Remotedesktopdatei für eine Rolleninstanz in einem Clouddienst ab.</span><span class="sxs-lookup"><span data-stu-id="a485c-106">Gets a remote desktop file for a role instance in a cloud service.</span></span>

## <span data-ttu-id="a485c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a485c-107">EXAMPLES</span></span>

### <span data-ttu-id="a485c-108">Beispiel 1: Herunterladen einer RDP-Datei</span><span class="sxs-lookup"><span data-stu-id="a485c-108">Example 1: Get an RDP file</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstanceRemoteDesktopFile -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0" -OutFile "C:\temp\ContosoFrontEnd_IN_0.rdp"
```

<span data-ttu-id="a485c-109">Dieser Befehl ruft eine RDP-Datei für die Rolleninstanz mit dem Namen ContosoFrontEnd IN 0 des Clouddiensts "ContosoCS" ab, die zur Ressourcengruppe \_ \_ "ContosOrg" gehört.</span><span class="sxs-lookup"><span data-stu-id="a485c-109">This command gets an RDP file for the role instance named ContosoFrontEnd\_IN\_0 of cloud Service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="a485c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a485c-110">PARAMETERS</span></span>

### <span data-ttu-id="a485c-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="a485c-111">-CloudServiceName</span></span>
<span data-ttu-id="a485c-112">.</span><span class="sxs-lookup"><span data-stu-id="a485c-112">.</span></span>

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

### <span data-ttu-id="a485c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a485c-113">-DefaultProfile</span></span>
<span data-ttu-id="a485c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a485c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a485c-115">-OutFile</span><span class="sxs-lookup"><span data-stu-id="a485c-115">-OutFile</span></span>
<span data-ttu-id="a485c-116">Pfad zum Schreiben einer Ausgabedatei in</span><span class="sxs-lookup"><span data-stu-id="a485c-116">Path to write output file to</span></span>

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

### <span data-ttu-id="a485c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a485c-117">-PassThru</span></span>
<span data-ttu-id="a485c-118">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="a485c-118">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a485c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a485c-119">-ResourceGroupName</span></span>
<span data-ttu-id="a485c-120">.</span><span class="sxs-lookup"><span data-stu-id="a485c-120">.</span></span>

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

### <span data-ttu-id="a485c-121">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="a485c-121">-RoleInstanceName</span></span>
<span data-ttu-id="a485c-122">Der Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="a485c-122">Name of the role instance.</span></span>

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

### <span data-ttu-id="a485c-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a485c-123">-SubscriptionId</span></span>
<span data-ttu-id="a485c-124">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a485c-124">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a485c-125">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="a485c-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a485c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a485c-126">CommonParameters</span></span>
<span data-ttu-id="a485c-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a485c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a485c-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a485c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a485c-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a485c-129">INPUTS</span></span>

## <span data-ttu-id="a485c-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a485c-130">OUTPUTS</span></span>

### <span data-ttu-id="a485c-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a485c-131">System.Boolean</span></span>

## <span data-ttu-id="a485c-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a485c-132">NOTES</span></span>

<span data-ttu-id="a485c-133">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a485c-133">ALIASES</span></span>

## <span data-ttu-id="a485c-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a485c-134">RELATED LINKS</span></span>

