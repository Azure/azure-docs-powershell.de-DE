---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
ms.openlocfilehash: 01b8283277c1d9592adbd8edfe6b883a4451ded9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663455"
---
# <span data-ttu-id="efa8b-101">Set-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="efa8b-101">Set-AzureRmDefault</span></span>

## <span data-ttu-id="efa8b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="efa8b-102">SYNOPSIS</span></span>
<span data-ttu-id="efa8b-103">Legt einen Standardwert im aktuellen Kontext fest.</span><span class="sxs-lookup"><span data-stu-id="efa8b-103">Sets a default in the current context</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efa8b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="efa8b-104">SYNTAX</span></span>

```
Set-AzureRmDefault [-ResourceGroupName <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efa8b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="efa8b-105">DESCRIPTION</span></span>
<span data-ttu-id="efa8b-106">Das Set-AzureRmDefault-Cmdlet fügt die Standardwerte im aktuellen Kontext hinzu oder ändert diese.</span><span class="sxs-lookup"><span data-stu-id="efa8b-106">The Set-AzureRmDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="efa8b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="efa8b-107">EXAMPLES</span></span>

### <span data-ttu-id="efa8b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="efa8b-108">Example 1</span></span>
```
PS C:\> Set-AzureRmDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="efa8b-109">Dieser Befehl legt die Standardressourcen Gruppe auf die vom Benutzer angegebene Ressourcengruppe fest.</span><span class="sxs-lookup"><span data-stu-id="efa8b-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="efa8b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="efa8b-110">PARAMETERS</span></span>

### <span data-ttu-id="efa8b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efa8b-111">-DefaultProfile</span></span>
<span data-ttu-id="efa8b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="efa8b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efa8b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="efa8b-113">-Force</span></span>
<span data-ttu-id="efa8b-114">Erstellen einer neuen Ressourcengruppe, wenn der angegebene Standard nicht vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="efa8b-114">Create a new resource group if specified default does not exist</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa8b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efa8b-115">-ResourceGroupName</span></span>
<span data-ttu-id="efa8b-116">Name der Ressourcengruppe, die als Standard eingestellt ist</span><span class="sxs-lookup"><span data-stu-id="efa8b-116">Name of the resource group being set as default</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efa8b-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="efa8b-117">-Confirm</span></span>
<span data-ttu-id="efa8b-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="efa8b-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa8b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efa8b-119">-WhatIf</span></span>
<span data-ttu-id="efa8b-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="efa8b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efa8b-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="efa8b-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa8b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efa8b-122">CommonParameters</span></span>
<span data-ttu-id="efa8b-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efa8b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efa8b-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efa8b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efa8b-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="efa8b-125">INPUTS</span></span>

### <span data-ttu-id="efa8b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="efa8b-126">System.String</span></span>

## <span data-ttu-id="efa8b-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="efa8b-127">OUTPUTS</span></span>

### <span data-ttu-id="efa8b-128">Microsoft. Azure. Management. Internal. resources. Models. ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="efa8b-128">Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroup</span></span>

## <span data-ttu-id="efa8b-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="efa8b-129">NOTES</span></span>

## <span data-ttu-id="efa8b-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="efa8b-130">RELATED LINKS</span></span>

