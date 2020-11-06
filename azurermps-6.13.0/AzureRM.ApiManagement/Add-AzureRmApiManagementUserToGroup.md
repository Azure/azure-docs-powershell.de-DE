---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
ms.openlocfilehash: abb86f40c9ac4a2ca04e0f14500df6c39e550dc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501262"
---
# <span data-ttu-id="be279-101">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="be279-101">Add-AzureRmApiManagementUserToGroup</span></span>

## <span data-ttu-id="be279-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="be279-102">SYNOPSIS</span></span>
<span data-ttu-id="be279-103">Fügt einen Benutzer zu einer Gruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="be279-103">Adds a user to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be279-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="be279-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be279-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be279-105">DESCRIPTION</span></span>
<span data-ttu-id="be279-106">Das Cmdlet **Add-AzureRmApiManagementUserToGroup** fügt einen Benutzer zu einer Gruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="be279-106">The **Add-AzureRmApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="be279-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be279-107">EXAMPLES</span></span>

### <span data-ttu-id="be279-108">Beispiel 1: Hinzufügen eines Benutzers zu einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="be279-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="be279-109">Dieser Befehl fügt einen vorhandenen Benutzer zu einer vorhandenen Gruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="be279-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="be279-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="be279-110">PARAMETERS</span></span>

### <span data-ttu-id="be279-111">-Context</span><span class="sxs-lookup"><span data-stu-id="be279-111">-Context</span></span>
<span data-ttu-id="be279-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="be279-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="be279-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="be279-113">This parameter is required.</span></span>

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

### <span data-ttu-id="be279-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be279-114">-DefaultProfile</span></span>
<span data-ttu-id="be279-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="be279-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be279-116">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="be279-116">-GroupId</span></span>
<span data-ttu-id="be279-117">Gibt die Gruppen-ID an.</span><span class="sxs-lookup"><span data-stu-id="be279-117">Specifies the group ID.</span></span>
<span data-ttu-id="be279-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="be279-118">This parameter is required.</span></span>

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

### <span data-ttu-id="be279-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be279-119">-PassThru</span></span>
<span data-ttu-id="be279-120">passthru</span><span class="sxs-lookup"><span data-stu-id="be279-120">passthru</span></span>

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

### <span data-ttu-id="be279-121">-UserID</span><span class="sxs-lookup"><span data-stu-id="be279-121">-UserId</span></span>
<span data-ttu-id="be279-122">Gibt die Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="be279-122">Specifies the user ID.</span></span>
<span data-ttu-id="be279-123">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="be279-123">This parameter is required.</span></span>

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

### <span data-ttu-id="be279-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be279-124">CommonParameters</span></span>
<span data-ttu-id="be279-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be279-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be279-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be279-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be279-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="be279-127">INPUTS</span></span>

### <span data-ttu-id="be279-128">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="be279-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="be279-129">System. String</span><span class="sxs-lookup"><span data-stu-id="be279-129">System.String</span></span>

### <span data-ttu-id="be279-130">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="be279-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="be279-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="be279-131">OUTPUTS</span></span>

### <span data-ttu-id="be279-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="be279-132">System.Boolean</span></span>

## <span data-ttu-id="be279-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="be279-133">NOTES</span></span>

## <span data-ttu-id="be279-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="be279-134">RELATED LINKS</span></span>

[<span data-ttu-id="be279-135">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="be279-135">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="be279-136">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="be279-136">Remove-AzureRmApiManagementUserFromGroup</span></span>](./Remove-AzureRmApiManagementUserFromGroup.md)


