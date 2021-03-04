---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzAllowedConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
ms.openlocfilehash: 211601ac2866dab85d46e61cba79ed074f79e22d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927608"
---
# <span data-ttu-id="d5c88-101">Get-AzAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="d5c88-101">Get-AzAllowedConnection</span></span>

## <span data-ttu-id="d5c88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5c88-102">SYNOPSIS</span></span>
<span data-ttu-id="d5c88-103">Wird zum Anzeigen des zulässigen Datenverkehrs zwischen Ressourcen für das Abonnement verwendet</span><span class="sxs-lookup"><span data-stu-id="d5c88-103">Used to display allowed traffic between resources for the subscription</span></span>


## <span data-ttu-id="d5c88-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5c88-104">SYNTAX</span></span>

### <span data-ttu-id="d5c88-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="d5c88-105">SubscriptionScope (Default)</span></span>
```
Get-AzAllowedConnection [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5c88-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="d5c88-106">ResourceGroupLevelResource</span></span>
```
Get-AzAllowedConnection -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5c88-107">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5c88-107">-ResourceId</span></span>
```
Get-AzAllowedConnection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5c88-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5c88-108">DESCRIPTION</span></span>
<span data-ttu-id="d5c88-109">Ruft die Liste aller möglichen Datenverkehre zwischen Ressourcen für das Abonnement und den Speicherort ab, basierend auf dem Verbindungstyp.</span><span class="sxs-lookup"><span data-stu-id="d5c88-109">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="d5c88-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d5c88-110">EXAMPLES</span></span>

### <span data-ttu-id="d5c88-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d5c88-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAllowedConnection
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/virtualMachines
Name:   Internal
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

### <span data-ttu-id="d5c88-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d5c88-112">Example 2</span></span>
```powershell
PS C:\> Get-AzAllowedConnection -ResourceGroupName "myService1" -Location "centralus" -Name "Internal"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/Internal
Name:   virtualMachines
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="d5c88-113">Ruft die Liste aller möglichen Datenverkehre zwischen Ressourcen für das Abonnement und den Speicherort ab, basierend auf dem Verbindungstyp.</span><span class="sxs-lookup"><span data-stu-id="d5c88-113">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="d5c88-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d5c88-114">PARAMETERS</span></span>

### <span data-ttu-id="d5c88-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5c88-115">-DefaultProfile</span></span>
<span data-ttu-id="d5c88-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5c88-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5c88-117">-Location</span><span class="sxs-lookup"><span data-stu-id="d5c88-117">-Location</span></span>
<span data-ttu-id="d5c88-118">Ort.</span><span class="sxs-lookup"><span data-stu-id="d5c88-118">Location.</span></span>

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

### <span data-ttu-id="d5c88-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d5c88-119">-Name</span></span>
<span data-ttu-id="d5c88-120">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="d5c88-120">Resource name.</span></span>

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

### <span data-ttu-id="d5c88-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5c88-121">-ResourceGroupName</span></span>
<span data-ttu-id="d5c88-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d5c88-122">Resource group name.</span></span>

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

### <span data-ttu-id="d5c88-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5c88-123">-ResourceId</span></span>
<span data-ttu-id="d5c88-124">ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="d5c88-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="d5c88-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5c88-125">CommonParameters</span></span>
<span data-ttu-id="d5c88-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5c88-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5c88-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5c88-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5c88-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d5c88-128">INPUTS</span></span>

### <span data-ttu-id="d5c88-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d5c88-129">System.String</span></span>

## <span data-ttu-id="d5c88-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d5c88-130">OUTPUTS</span></span>

### <span data-ttu-id="d5c88-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="d5c88-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span></span>


## <span data-ttu-id="d5c88-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d5c88-132">NOTES</span></span>

## <span data-ttu-id="d5c88-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d5c88-133">RELATED LINKS</span></span>
