---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzAllowedConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
ms.openlocfilehash: 3a604cbdda30612016763fef75fcf62e0c8e36f7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298091"
---
# <span data-ttu-id="9e254-101">Get-AzAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="9e254-101">Get-AzAllowedConnection</span></span>

## <span data-ttu-id="9e254-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e254-102">SYNOPSIS</span></span>
<span data-ttu-id="9e254-103">Wird zum Anzeigen des zulässigen Datenverkehrs zwischen Ressourcen für das Abonnement verwendet</span><span class="sxs-lookup"><span data-stu-id="9e254-103">Used to display allowed traffic between resources for the subscription</span></span>


## <span data-ttu-id="9e254-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e254-104">SYNTAX</span></span>

### <span data-ttu-id="9e254-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="9e254-105">SubscriptionScope (Default)</span></span>
```
Get-AzAllowedConnection [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e254-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="9e254-106">ResourceGroupLevelResource</span></span>
```
Get-AzAllowedConnection -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e254-107">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e254-107">-ResourceId</span></span>
```
Get-AzAllowedConnection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e254-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e254-108">DESCRIPTION</span></span>
<span data-ttu-id="9e254-109">Ruft die Liste des möglichen Datenverkehrs zwischen Ressourcen für das Abonnement und den Standort ab, basierend auf dem Verbindungstyp.</span><span class="sxs-lookup"><span data-stu-id="9e254-109">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="9e254-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9e254-110">EXAMPLES</span></span>

### <span data-ttu-id="9e254-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9e254-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAllowedConnection
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/virtualMachines
Name:   Internal
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

### <span data-ttu-id="9e254-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9e254-112">Example 2</span></span>
```powershell
PS C:\> Get-AzAllowedConnection -ResourceGroupName "myService1" -Location "centralus" -Name "Internal"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/Internal
Name:   virtualMachines
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="9e254-113">Ruft die Liste des möglichen Datenverkehrs zwischen Ressourcen für das Abonnement und den Standort ab, basierend auf dem Verbindungstyp.</span><span class="sxs-lookup"><span data-stu-id="9e254-113">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="9e254-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e254-114">PARAMETERS</span></span>

### <span data-ttu-id="9e254-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e254-115">-DefaultProfile</span></span>
<span data-ttu-id="9e254-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e254-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e254-117">-Location</span><span class="sxs-lookup"><span data-stu-id="9e254-117">-Location</span></span>
<span data-ttu-id="9e254-118">"Ort" aus.</span><span class="sxs-lookup"><span data-stu-id="9e254-118">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e254-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9e254-119">-Name</span></span>
<span data-ttu-id="9e254-120">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="9e254-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e254-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e254-121">-ResourceGroupName</span></span>
<span data-ttu-id="9e254-122">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="9e254-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e254-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e254-123">-ResourceId</span></span>
<span data-ttu-id="9e254-124">DIE ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="9e254-124">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e254-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e254-125">CommonParameters</span></span>
<span data-ttu-id="9e254-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e254-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e254-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e254-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e254-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9e254-128">INPUTS</span></span>

### <span data-ttu-id="9e254-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9e254-129">System.String</span></span>

## <span data-ttu-id="9e254-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9e254-130">OUTPUTS</span></span>

### <span data-ttu-id="9e254-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="9e254-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span></span>


## <span data-ttu-id="9e254-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9e254-132">NOTES</span></span>

## <span data-ttu-id="9e254-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9e254-133">RELATED LINKS</span></span>
