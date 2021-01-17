---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
ms.openlocfilehash: e44b9a5c497aba5533d53acdc9aab31cb5ece703
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373118"
---
# <span data-ttu-id="81f32-101">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="81f32-101">Set-AzAutomationCredential</span></span>

## <span data-ttu-id="81f32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81f32-102">SYNOPSIS</span></span>
<span data-ttu-id="81f32-103">Ändert die Anmeldeinformationen für die Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="81f32-103">Modifies an Automation credential.</span></span>

## <span data-ttu-id="81f32-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81f32-104">SYNTAX</span></span>

```
Set-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81f32-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81f32-105">DESCRIPTION</span></span>
<span data-ttu-id="81f32-106">Das **Cmdlet "Set-AzAutomationCredential"** ändert anmeldeinformationen als **"PSCredential"-Objekt** in der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="81f32-106">The **Set-AzAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="81f32-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="81f32-107">EXAMPLES</span></span>

### <span data-ttu-id="81f32-108">Beispiel 1: Aktualisieren von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="81f32-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="81f32-109">Der erste Befehl weist der Variablen "$User" einen Benutzernamen zu.</span><span class="sxs-lookup"><span data-stu-id="81f32-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="81f32-110">Mit dem zweiten Befehl wird ein Nur-Text-Kennwort mithilfe des Cmdlets ConvertTo-SecureString sichere Zeichenfolge konvertiert.</span><span class="sxs-lookup"><span data-stu-id="81f32-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="81f32-111">Der Befehl speichert dieses Objekt in der $Password Variable.</span><span class="sxs-lookup"><span data-stu-id="81f32-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="81f32-112">Der dritte Befehl erstellt anmeldeinformationen basierend auf $User und $Password und speichert sie dann in $Credential Variable.</span><span class="sxs-lookup"><span data-stu-id="81f32-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="81f32-113">Der letzte Befehl ändert die Automatisierungsanmeldeinformationen namens "ContosoCredential", um die Anmeldeinformationen in der $Credential.</span><span class="sxs-lookup"><span data-stu-id="81f32-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="81f32-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81f32-114">PARAMETERS</span></span>

### <span data-ttu-id="81f32-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="81f32-115">-AutomationAccountName</span></span>
<span data-ttu-id="81f32-116">Gibt den Namen des Automatisierungskontos an, für das dieses Cmdlet Anmeldeinformationen ändert.</span><span class="sxs-lookup"><span data-stu-id="81f32-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81f32-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81f32-117">-DefaultProfile</span></span>
<span data-ttu-id="81f32-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="81f32-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81f32-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81f32-119">-Description</span></span>
<span data-ttu-id="81f32-120">Gibt eine Beschreibung der Anmeldeinformationen an, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="81f32-120">Specifies a description for the credential that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81f32-121">-Name</span><span class="sxs-lookup"><span data-stu-id="81f32-121">-Name</span></span>
<span data-ttu-id="81f32-122">Gibt den Namen der Anmeldeinformationen an, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="81f32-122">Specifies the name of the credential that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81f32-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81f32-123">-ResourceGroupName</span></span>
<span data-ttu-id="81f32-124">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet Anmeldeinformationen ändert.</span><span class="sxs-lookup"><span data-stu-id="81f32-124">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="81f32-125">-Value</span><span class="sxs-lookup"><span data-stu-id="81f32-125">-Value</span></span>
<span data-ttu-id="81f32-126">Gibt die Anmeldeinformationen als ein **"PSCredential"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="81f32-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81f32-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81f32-127">CommonParameters</span></span>
<span data-ttu-id="81f32-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81f32-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81f32-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81f32-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81f32-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="81f32-130">INPUTS</span></span>

### <span data-ttu-id="81f32-131">System.String</span><span class="sxs-lookup"><span data-stu-id="81f32-131">System.String</span></span>

### <span data-ttu-id="81f32-132">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="81f32-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="81f32-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="81f32-133">OUTPUTS</span></span>

### <span data-ttu-id="81f32-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="81f32-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="81f32-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="81f32-135">NOTES</span></span>

## <span data-ttu-id="81f32-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="81f32-136">RELATED LINKS</span></span>

[<span data-ttu-id="81f32-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="81f32-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="81f32-138">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="81f32-138">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="81f32-139">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="81f32-139">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)


