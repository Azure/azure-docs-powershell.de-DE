---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 03073dc6116595c93b2c25d30b38c5467482903c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948091"
---
# <span data-ttu-id="f1955-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="f1955-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="f1955-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1955-102">SYNOPSIS</span></span>
<span data-ttu-id="f1955-103">Entfernt einen Benutzer aus einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f1955-103">Removes a user from a group.</span></span>

## <span data-ttu-id="f1955-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1955-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1955-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1955-105">DESCRIPTION</span></span>
<span data-ttu-id="f1955-106">Das **Cmdlet Remove-AzApiManagementUserFromGroup** entfernt einen Benutzer aus einer vorhandenen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f1955-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="f1955-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f1955-107">EXAMPLES</span></span>

### <span data-ttu-id="f1955-108">Beispiel 1: Entfernen eines Benutzers aus einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="f1955-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="f1955-109">Mit diesem Befehl wird ein Benutzer aus einer Gruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="f1955-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="f1955-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f1955-110">PARAMETERS</span></span>

### <span data-ttu-id="f1955-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f1955-111">-Context</span></span>
<span data-ttu-id="f1955-112">Gibt ein **PsApiManagementContext-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="f1955-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f1955-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f1955-113">This parameter is required.</span></span>

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

### <span data-ttu-id="f1955-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1955-114">-DefaultProfile</span></span>
<span data-ttu-id="f1955-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1955-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1955-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="f1955-116">-GroupId</span></span>
<span data-ttu-id="f1955-117">Gibt die ID der Gruppe an, aus der ein Benutzer entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1955-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="f1955-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1955-118">-PassThru</span></span>
<span data-ttu-id="f1955-119">Gibt an, dass dieses Cmdlet einen Wert von $True , wenn es erfolgreich ist, oder einen Wert von $False zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f1955-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="f1955-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="f1955-120">-UserId</span></span>
<span data-ttu-id="f1955-121">Gibt die ID des Benutzers an, der aus der Gruppe entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1955-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="f1955-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1955-122">CommonParameters</span></span>
<span data-ttu-id="f1955-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1955-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1955-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1955-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1955-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f1955-125">INPUTS</span></span>

### <span data-ttu-id="f1955-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f1955-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f1955-127">System.String</span><span class="sxs-lookup"><span data-stu-id="f1955-127">System.String</span></span>

### <span data-ttu-id="f1955-128">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f1955-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f1955-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f1955-129">OUTPUTS</span></span>

### <span data-ttu-id="f1955-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f1955-130">System.Boolean</span></span>

## <span data-ttu-id="f1955-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f1955-131">NOTES</span></span>

## <span data-ttu-id="f1955-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f1955-132">RELATED LINKS</span></span>

[<span data-ttu-id="f1955-133">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="f1955-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="f1955-134">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f1955-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


