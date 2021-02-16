---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
ms.openlocfilehash: 27e6be451d6141e322c47b2a84a28baf115839ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155009"
---
# <span data-ttu-id="9ee98-101">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="9ee98-101">Add-AzApiManagementUserToGroup</span></span>

## <span data-ttu-id="9ee98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ee98-102">SYNOPSIS</span></span>
<span data-ttu-id="9ee98-103">Fügt einen Benutzer zu einer Gruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="9ee98-103">Adds a user to a group.</span></span>

## <span data-ttu-id="9ee98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ee98-104">SYNTAX</span></span>

```
Add-AzApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ee98-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ee98-105">DESCRIPTION</span></span>
<span data-ttu-id="9ee98-106">Das **Cmdlet "Add-AzApiManagementUserToGroup"** fügt einen Benutzer zu einer Gruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="9ee98-106">The **Add-AzApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="9ee98-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9ee98-107">EXAMPLES</span></span>

### <span data-ttu-id="9ee98-108">Beispiel 1: Hinzufügen eines Benutzers zu einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="9ee98-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="9ee98-109">Mit diesem Befehl wird einer vorhandenen Gruppe ein vorhandener Benutzer hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="9ee98-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="9ee98-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ee98-110">PARAMETERS</span></span>

### <span data-ttu-id="9ee98-111">-Context</span><span class="sxs-lookup"><span data-stu-id="9ee98-111">-Context</span></span>
<span data-ttu-id="9ee98-112">Gibt ein **"PsApiManagementContext"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="9ee98-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="9ee98-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9ee98-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee98-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ee98-114">-DefaultProfile</span></span>
<span data-ttu-id="9ee98-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ee98-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ee98-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="9ee98-116">-GroupId</span></span>
<span data-ttu-id="9ee98-117">Gibt die Gruppen-ID an.</span><span class="sxs-lookup"><span data-stu-id="9ee98-117">Specifies the group ID.</span></span>
<span data-ttu-id="9ee98-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9ee98-118">This parameter is required.</span></span>

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

### <span data-ttu-id="9ee98-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ee98-119">-PassThru</span></span>
<span data-ttu-id="9ee98-120">passthru</span><span class="sxs-lookup"><span data-stu-id="9ee98-120">passthru</span></span>

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

### <span data-ttu-id="9ee98-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="9ee98-121">-UserId</span></span>
<span data-ttu-id="9ee98-122">Gibt die Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="9ee98-122">Specifies the user ID.</span></span>
<span data-ttu-id="9ee98-123">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9ee98-123">This parameter is required.</span></span>

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

### <span data-ttu-id="9ee98-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ee98-124">CommonParameters</span></span>
<span data-ttu-id="9ee98-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ee98-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ee98-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ee98-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ee98-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9ee98-127">INPUTS</span></span>

### <span data-ttu-id="9ee98-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9ee98-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9ee98-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9ee98-129">System.String</span></span>

### <span data-ttu-id="9ee98-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9ee98-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9ee98-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9ee98-131">OUTPUTS</span></span>

### <span data-ttu-id="9ee98-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9ee98-132">System.Boolean</span></span>

## <span data-ttu-id="9ee98-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9ee98-133">NOTES</span></span>

## <span data-ttu-id="9ee98-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9ee98-134">RELATED LINKS</span></span>

[<span data-ttu-id="9ee98-135">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="9ee98-135">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="9ee98-136">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="9ee98-136">Remove-AzApiManagementUserFromGroup</span></span>](./Remove-AzApiManagementUserFromGroup.md)


