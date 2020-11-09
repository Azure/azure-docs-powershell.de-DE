---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
ms.openlocfilehash: 27e6be451d6141e322c47b2a84a28baf115839ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299967"
---
# <span data-ttu-id="a281b-101">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="a281b-101">Add-AzApiManagementUserToGroup</span></span>

## <span data-ttu-id="a281b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a281b-102">SYNOPSIS</span></span>
<span data-ttu-id="a281b-103">Fügt einen Benutzer zu einer Gruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="a281b-103">Adds a user to a group.</span></span>

## <span data-ttu-id="a281b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a281b-104">SYNTAX</span></span>

```
Add-AzApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a281b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a281b-105">DESCRIPTION</span></span>
<span data-ttu-id="a281b-106">Das Cmdlet **Add-AzApiManagementUserToGroup** fügt einen Benutzer zu einer Gruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="a281b-106">The **Add-AzApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="a281b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a281b-107">EXAMPLES</span></span>

### <span data-ttu-id="a281b-108">Beispiel 1: Hinzufügen eines Benutzers zu einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="a281b-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="a281b-109">Dieser Befehl fügt einen vorhandenen Benutzer zu einer vorhandenen Gruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="a281b-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="a281b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a281b-110">PARAMETERS</span></span>

### <span data-ttu-id="a281b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a281b-111">-Context</span></span>
<span data-ttu-id="a281b-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a281b-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="a281b-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a281b-113">This parameter is required.</span></span>

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

### <span data-ttu-id="a281b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a281b-114">-DefaultProfile</span></span>
<span data-ttu-id="a281b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a281b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a281b-116">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="a281b-116">-GroupId</span></span>
<span data-ttu-id="a281b-117">Gibt die Gruppen-ID an.</span><span class="sxs-lookup"><span data-stu-id="a281b-117">Specifies the group ID.</span></span>
<span data-ttu-id="a281b-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a281b-118">This parameter is required.</span></span>

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

### <span data-ttu-id="a281b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a281b-119">-PassThru</span></span>
<span data-ttu-id="a281b-120">passthru</span><span class="sxs-lookup"><span data-stu-id="a281b-120">passthru</span></span>

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

### <span data-ttu-id="a281b-121">-UserID</span><span class="sxs-lookup"><span data-stu-id="a281b-121">-UserId</span></span>
<span data-ttu-id="a281b-122">Gibt die Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="a281b-122">Specifies the user ID.</span></span>
<span data-ttu-id="a281b-123">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a281b-123">This parameter is required.</span></span>

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

### <span data-ttu-id="a281b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a281b-124">CommonParameters</span></span>
<span data-ttu-id="a281b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a281b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a281b-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a281b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a281b-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a281b-127">INPUTS</span></span>

### <span data-ttu-id="a281b-128">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a281b-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a281b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a281b-129">System.String</span></span>

### <span data-ttu-id="a281b-130">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="a281b-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a281b-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a281b-131">OUTPUTS</span></span>

### <span data-ttu-id="a281b-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a281b-132">System.Boolean</span></span>

## <span data-ttu-id="a281b-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="a281b-133">NOTES</span></span>

## <span data-ttu-id="a281b-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a281b-134">RELATED LINKS</span></span>

[<span data-ttu-id="a281b-135">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a281b-135">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="a281b-136">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="a281b-136">Remove-AzApiManagementUserFromGroup</span></span>](./Remove-AzApiManagementUserFromGroup.md)


