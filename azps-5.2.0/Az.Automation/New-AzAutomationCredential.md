---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
ms.openlocfilehash: a0b23cc5e16a723364d234eb2ee9723f291ee5e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373553"
---
# <span data-ttu-id="e12c6-101">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e12c6-101">New-AzAutomationCredential</span></span>

## <span data-ttu-id="e12c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e12c6-102">SYNOPSIS</span></span>
<span data-ttu-id="e12c6-103">Erstellt ein Automatisierungsanmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="e12c6-103">Creates an Automation credential.</span></span>

## <span data-ttu-id="e12c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e12c6-104">SYNTAX</span></span>

```
New-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e12c6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e12c6-105">DESCRIPTION</span></span>
<span data-ttu-id="e12c6-106">Das **Cmdlet "New-AzAutomationCredential"** erstellt anmeldeinformationen als **"PSCredential"-Objekt** in der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="e12c6-106">The **New-AzAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="e12c6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e12c6-107">EXAMPLES</span></span>

### <span data-ttu-id="e12c6-108">Beispiel 1: Erstellen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="e12c6-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e12c6-109">Der erste Befehl weist der Variablen "$User" einen Benutzernamen zu.</span><span class="sxs-lookup"><span data-stu-id="e12c6-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="e12c6-110">Mit dem zweiten Befehl wird ein Nur-Text-Kennwort mithilfe des Cmdlets ConvertTo-SecureString sichere Zeichenfolge konvertiert.</span><span class="sxs-lookup"><span data-stu-id="e12c6-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="e12c6-111">Der Befehl speichert dieses Objekt in der $Password Variable.</span><span class="sxs-lookup"><span data-stu-id="e12c6-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="e12c6-112">Der dritte Befehl erstellt anmeldeinformationen basierend auf $User und $Password und speichert sie dann in $Credential Variable.</span><span class="sxs-lookup"><span data-stu-id="e12c6-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="e12c6-113">Der letzte Befehl erstellt eine Automatisierungsanmeldeinformation namens "ContosoCredential", die $Credential.</span><span class="sxs-lookup"><span data-stu-id="e12c6-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="e12c6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e12c6-114">PARAMETERS</span></span>

### <span data-ttu-id="e12c6-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e12c6-115">-AutomationAccountName</span></span>
<span data-ttu-id="e12c6-116">Gibt den Namen des Automatisierungskontos an, in dem dieses Cmdlet die Anmeldeinformationen speichert.</span><span class="sxs-lookup"><span data-stu-id="e12c6-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="e12c6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e12c6-117">-DefaultProfile</span></span>
<span data-ttu-id="e12c6-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e12c6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e12c6-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e12c6-119">-Description</span></span>
<span data-ttu-id="e12c6-120">Gibt eine Beschreibung für die Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="e12c6-120">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="e12c6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e12c6-121">-Name</span></span>
<span data-ttu-id="e12c6-122">Gibt einen Namen für die Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="e12c6-122">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="e12c6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e12c6-123">-ResourceGroupName</span></span>
<span data-ttu-id="e12c6-124">Gibt eine Beschreibung für die Ressourcengruppe an, für die dieses Cmdlet Anmeldeinformationen erstellt.</span><span class="sxs-lookup"><span data-stu-id="e12c6-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="e12c6-125">-Value</span><span class="sxs-lookup"><span data-stu-id="e12c6-125">-Value</span></span>
<span data-ttu-id="e12c6-126">Gibt die Anmeldeinformationen als ein **"PSCredential"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="e12c6-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e12c6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e12c6-127">CommonParameters</span></span>
<span data-ttu-id="e12c6-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e12c6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e12c6-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e12c6-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e12c6-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e12c6-130">INPUTS</span></span>

### <span data-ttu-id="e12c6-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e12c6-131">System.String</span></span>

### <span data-ttu-id="e12c6-132">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="e12c6-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="e12c6-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e12c6-133">OUTPUTS</span></span>

### <span data-ttu-id="e12c6-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="e12c6-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="e12c6-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e12c6-135">NOTES</span></span>

## <span data-ttu-id="e12c6-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e12c6-136">RELATED LINKS</span></span>

[<span data-ttu-id="e12c6-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e12c6-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="e12c6-138">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e12c6-138">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="e12c6-139">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e12c6-139">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


