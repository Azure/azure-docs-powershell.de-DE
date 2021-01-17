---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
ms.openlocfilehash: 1069365bb04cdf9a6d873e6fa86c61619b6d0dab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470962"
---
# <span data-ttu-id="3ca20-101">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3ca20-101">Remove-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="3ca20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ca20-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca20-103">Löscht ein Cognitive Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="3ca20-103">Deletes a Cognitive Services account.</span></span>

## <span data-ttu-id="3ca20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ca20-104">SYNTAX</span></span>

```
Remove-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ca20-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ca20-105">DESCRIPTION</span></span>
<span data-ttu-id="3ca20-106">Das **Cmdlet "Remove-AzCognitiveServicesAccount"** löscht das angegebene Cognitive Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="3ca20-106">The **Remove-AzCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="3ca20-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3ca20-107">EXAMPLES</span></span>

### <span data-ttu-id="3ca20-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3ca20-108">Example 1</span></span>
<span data-ttu-id="3ca20-109">Dieser Befehl gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="3ca20-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="3ca20-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ca20-110">PARAMETERS</span></span>

### <span data-ttu-id="3ca20-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca20-111">-DefaultProfile</span></span>
<span data-ttu-id="3ca20-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3ca20-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ca20-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3ca20-113">-Force</span></span>
<span data-ttu-id="3ca20-114">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="3ca20-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca20-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3ca20-115">-Name</span></span>
<span data-ttu-id="3ca20-116">Gibt den Namen des zu löschenden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="3ca20-116">Specifies the name of the account to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ca20-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ca20-117">-ResourceGroupName</span></span>
<span data-ttu-id="3ca20-118">Gibt den Namen der Ressourcengruppe an, der das Cognitive Services-Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3ca20-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ca20-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ca20-119">-Confirm</span></span>
<span data-ttu-id="3ca20-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3ca20-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca20-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3ca20-121">-WhatIf</span></span>
<span data-ttu-id="3ca20-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3ca20-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ca20-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3ca20-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca20-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca20-124">CommonParameters</span></span>
<span data-ttu-id="3ca20-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ca20-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca20-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ca20-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca20-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3ca20-127">INPUTS</span></span>

### <span data-ttu-id="3ca20-128">System.String</span><span class="sxs-lookup"><span data-stu-id="3ca20-128">System.String</span></span>

## <span data-ttu-id="3ca20-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3ca20-129">OUTPUTS</span></span>

### <span data-ttu-id="3ca20-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="3ca20-130">System.Void</span></span>

## <span data-ttu-id="3ca20-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3ca20-131">NOTES</span></span>

## <span data-ttu-id="3ca20-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3ca20-132">RELATED LINKS</span></span>

[<span data-ttu-id="3ca20-133">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3ca20-133">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="3ca20-134">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3ca20-134">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="3ca20-135">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3ca20-135">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


