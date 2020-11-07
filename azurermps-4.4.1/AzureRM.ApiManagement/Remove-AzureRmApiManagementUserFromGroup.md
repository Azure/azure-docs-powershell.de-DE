---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
ms.openlocfilehash: 2867e8eec65de040a0da61a1af960abc9797bb18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663618"
---
# <span data-ttu-id="9f172-101">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="9f172-101">Remove-AzureRmApiManagementUserFromGroup</span></span>

## <span data-ttu-id="9f172-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9f172-102">SYNOPSIS</span></span>
<span data-ttu-id="9f172-103">Entfernt einen Benutzer aus einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="9f172-103">Removes a user from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f172-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f172-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f172-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f172-105">DESCRIPTION</span></span>
<span data-ttu-id="9f172-106">Das Cmdlet **Remove-AzureRmApiManagementUserFromGroup** entfernt einen Benutzer aus einer vorhandenen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="9f172-106">The **Remove-AzureRmApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="9f172-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9f172-107">EXAMPLES</span></span>

### <span data-ttu-id="9f172-108">Beispiel 1: Entfernen eines Benutzers aus einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="9f172-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>Remove-AzureRmApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="9f172-109">Dieser Befehl entfernt einen Benutzer aus einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="9f172-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="9f172-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f172-110">PARAMETERS</span></span>

### <span data-ttu-id="9f172-111">-Context</span><span class="sxs-lookup"><span data-stu-id="9f172-111">-Context</span></span>
<span data-ttu-id="9f172-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="9f172-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="9f172-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9f172-113">This parameter is required.</span></span>

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

### <span data-ttu-id="9f172-114">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="9f172-114">-GroupId</span></span>
<span data-ttu-id="9f172-115">Gibt die ID der Gruppe an, aus der ein Benutzer entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9f172-115">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="9f172-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f172-116">-PassThru</span></span>
<span data-ttu-id="9f172-117">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, wenn dies erfolgreich ist, oder einen Wert von $false, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="9f172-117">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="9f172-118">-UserID</span><span class="sxs-lookup"><span data-stu-id="9f172-118">-UserId</span></span>
<span data-ttu-id="9f172-119">Gibt die ID des Benutzers an, der aus der Gruppe entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9f172-119">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="9f172-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f172-120">-DefaultProfile</span></span>
<span data-ttu-id="9f172-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9f172-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f172-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f172-122">CommonParameters</span></span>
<span data-ttu-id="9f172-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f172-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f172-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f172-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f172-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9f172-125">INPUTS</span></span>

## <span data-ttu-id="9f172-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9f172-126">OUTPUTS</span></span>

### <span data-ttu-id="9f172-127">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9f172-127">System.Boolean</span></span>

## <span data-ttu-id="9f172-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="9f172-128">NOTES</span></span>

## <span data-ttu-id="9f172-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9f172-129">RELATED LINKS</span></span>

[<span data-ttu-id="9f172-130">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="9f172-130">Add-AzureRmApiManagementUserToGroup</span></span>](./Add-AzureRmApiManagementUserToGroup.md)

[<span data-ttu-id="9f172-131">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="9f172-131">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


