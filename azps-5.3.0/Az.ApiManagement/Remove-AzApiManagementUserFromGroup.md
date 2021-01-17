---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 220af172efa397de2fc0fafa7597c2b6e29dae60
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381897"
---
# <span data-ttu-id="04317-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="04317-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="04317-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04317-102">SYNOPSIS</span></span>
<span data-ttu-id="04317-103">Entfernt einen Benutzer aus einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="04317-103">Removes a user from a group.</span></span>

## <span data-ttu-id="04317-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04317-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04317-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04317-105">DESCRIPTION</span></span>
<span data-ttu-id="04317-106">Das **Cmdlet "Remove-AzApiManagementUserFromGroup"** entfernt einen Benutzer aus einer vorhandenen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="04317-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="04317-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="04317-107">EXAMPLES</span></span>

### <span data-ttu-id="04317-108">Beispiel 1: Entfernen eines Benutzers aus einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="04317-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="04317-109">Mit diesem Befehl wird ein Benutzer aus einer Gruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="04317-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="04317-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04317-110">PARAMETERS</span></span>

### <span data-ttu-id="04317-111">-Context</span><span class="sxs-lookup"><span data-stu-id="04317-111">-Context</span></span>
<span data-ttu-id="04317-112">Gibt ein **"PsApiManagementContext"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="04317-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="04317-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="04317-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04317-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04317-114">-DefaultProfile</span></span>
<span data-ttu-id="04317-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="04317-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04317-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="04317-116">-GroupId</span></span>
<span data-ttu-id="04317-117">Gibt die ID der Gruppe an, aus der ein Benutzer entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="04317-117">Specifies the ID of the group from which to remove a user.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04317-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04317-118">-PassThru</span></span>
<span data-ttu-id="04317-119">Gibt an, dass dieses Cmdlet den Wert "$True" zurückgibt, wenn es erfolgreich ist, oder den Wert "$False" zurück.</span><span class="sxs-lookup"><span data-stu-id="04317-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04317-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="04317-120">-UserId</span></span>
<span data-ttu-id="04317-121">Gibt die ID des Benutzers an, der aus der Gruppe entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="04317-121">Specifies the ID of the user to remove from the group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04317-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04317-122">CommonParameters</span></span>
<span data-ttu-id="04317-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04317-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04317-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04317-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04317-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="04317-125">INPUTS</span></span>

### <span data-ttu-id="04317-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="04317-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="04317-127">System.String</span><span class="sxs-lookup"><span data-stu-id="04317-127">System.String</span></span>

### <span data-ttu-id="04317-128">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="04317-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="04317-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="04317-129">OUTPUTS</span></span>

### <span data-ttu-id="04317-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="04317-130">System.Boolean</span></span>

## <span data-ttu-id="04317-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="04317-131">NOTES</span></span>

## <span data-ttu-id="04317-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="04317-132">RELATED LINKS</span></span>

[<span data-ttu-id="04317-133">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="04317-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="04317-134">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="04317-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


