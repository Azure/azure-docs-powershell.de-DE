---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmDefault.md
ms.openlocfilehash: 20d66412002e8feb1b4007608091cdbf0422b6c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502538"
---
# <span data-ttu-id="6edf5-101">Get-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="6edf5-101">Get-AzureRmDefault</span></span>

## <span data-ttu-id="6edf5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6edf5-102">SYNOPSIS</span></span>
<span data-ttu-id="6edf5-103">Rufen Sie die vom Benutzer im aktuellen Kontext gesetzten Standardwerte ab.</span><span class="sxs-lookup"><span data-stu-id="6edf5-103">Get the defaults set by the user in the current context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6edf5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6edf5-104">SYNTAX</span></span>

```
Get-AzureRmDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6edf5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6edf5-105">DESCRIPTION</span></span>
<span data-ttu-id="6edf5-106">Das Get-AzureRmDefault-Cmdlet ruft die Ressourcengruppe ab, die der Benutzer im aktuellen Kontext als Standard festgesetzt hat.</span><span class="sxs-lookup"><span data-stu-id="6edf5-106">The Get-AzureRmDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="6edf5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6edf5-107">EXAMPLES</span></span>

### <span data-ttu-id="6edf5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6edf5-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="6edf5-109">Dieser Befehl gibt die aktuellen Standardwerte zurück, wenn Standardwerte gesetzt sind, oder gibt Nothing zurück, wenn kein Standardwert gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="6edf5-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="6edf5-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6edf5-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="6edf5-111">Dieser Befehl gibt die aktuelle Standardressourcen Gruppe zurück, wenn ein Standardsatz vorhanden ist, oder gibt Nothing zurück, wenn kein Standardwert gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="6edf5-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="6edf5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6edf5-112">PARAMETERS</span></span>

### <span data-ttu-id="6edf5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6edf5-113">-DefaultProfile</span></span>
<span data-ttu-id="6edf5-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6edf5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6edf5-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6edf5-115">-ResourceGroup</span></span>
<span data-ttu-id="6edf5-116">Standardressourcen Gruppe anzeigen</span><span class="sxs-lookup"><span data-stu-id="6edf5-116">Display Default Resource Group</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6edf5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6edf5-117">CommonParameters</span></span>
<span data-ttu-id="6edf5-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6edf5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6edf5-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6edf5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6edf5-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6edf5-120">INPUTS</span></span>

### <span data-ttu-id="6edf5-121">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="6edf5-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6edf5-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6edf5-122">OUTPUTS</span></span>

### <span data-ttu-id="6edf5-123">Microsoft. Azure. Management. Internal. resources. Models. ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6edf5-123">Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroup</span></span>

## <span data-ttu-id="6edf5-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="6edf5-124">NOTES</span></span>

## <span data-ttu-id="6edf5-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6edf5-125">RELATED LINKS</span></span>

